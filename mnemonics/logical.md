# Logical
Key:
````
r -> register (cl, cx, ecx, or r1b, r1w, r1d)
m -> memory address ([bx])
i -> immediate value (0x03, 0x0003, 0x00000003)
8 -> operand size of 8 bits (cl, 0x03)
16 -> operand size of 16 bits (cx, 0x0003)
32 -> operand size of 32 bits (ecx, 0x00000003)
carry -> bit from carry flag
````
<table>
   <thead>
      <tr><th rowspan=2>Mnemonic</th><th rowspan=2>Description</th><th colspan=2>Operands</th><th rowspan=2>Operation</th></tr>
      <tr><th>dest</th><th>source</th></tr>
   </thead>
   <tbody>
      <tr><td rowspan=6>and</td><td rowspan=6>AND (Logical Conjunction)</td><td>r8</td><td>r/m/i8</td><td rowspan=6>dest = dest && source</td></tr>
      <tr><td>m8</td><td>r/i8</td></tr>
      <tr><td>r16</td><td>r/m/i16</td></tr>
      <tr><td>m16</td><td>r/i16</td></tr>
      <tr><td>r32</td><td>r/m/i32</td></tr>
      <tr><td>m32</td><td>r/i32</td></tr>
      <tr><td rowspan=3>not</td><td rowspan=3>NOT (1's Complement)</td><td colspan=2>r/m8</td><td rowspan=3>operand = !operand</td></tr>
      <tr><td colspan=2>r/m16</td></tr>
      <tr><td colspan=2>r/m32</td></tr>
      <tr><td rowspan=6>or</td><td rowspan=6>OR (Logical Inclusive Disjunction)</td><td>r8</td><td>r/m/i8</td><td rowspan=6>dest = dest || source</td></tr>
      <tr><td>m8</td><td>r/i8</td></tr>
      <tr><td>r16</td><td>r/m/i16</td></tr>
      <tr><td>m16</td><td>r/i16</td></tr>
      <tr><td>r32</td><td>r/m/i32</td></tr>
      <tr><td>m32</td><td>r/i32</td></tr>
      <tr><td rowspan=3>test</td><td rowspan=3>Temporary AND (Logical Conjunction)</td><td>r/m8</td><td>r/i8</td><td rowspan=3>Flags are updated, but the source remains the original value.</td></tr>
      <tr><td>r/m16</td><td>r/i16</td></tr>
      <tr><td>r/m32</td><td>r/i32</td></tr>
      <tr><td rowspan=6>xor</td><td rowspan=6>XOR (Logical Exclusive Disjunction)</td><td>r8</td><td>r/m/i8</td><td rowspan=6>dest = dest &oplus; source</td></tr>
      <tr><td>m8</td><td>r/i8</td></tr>
      <tr><td>r16</td><td>r/m/i16</td></tr>
      <tr><td>m16</td><td>r/i16</td></tr>
      <tr><td>r32</td><td>r/m/i32</td></tr>
      <tr><td>m32</td><td>r/i32</td></tr>
   </tbody>
</table>

