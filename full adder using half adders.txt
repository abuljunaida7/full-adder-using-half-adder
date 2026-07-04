module full_adder_using_half_adder(input a_ha,b_ha,cin_ha,output sum_ha,carry_ha

    );
    wire w1,w2,w3;
    half_adder ha1(.a(a_ha),.b(b_ha),.sum(w1),.carry(w2));
    half_adder ha2(.a(w1),.b(cin_ha),.sum(sum_ha),.carry(w3));
    or o1(carry_ha,w2,w3);
endmodule
