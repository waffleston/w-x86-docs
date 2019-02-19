# Arithmetic
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
      <tr><td rowspan=6>adc</td><td rowspan=6>Add Integers with Carry</td><td>r8</td><td>r/m/i8</td><td rowspan=6>dest = dest + source + carry</td></tr>
      <tr><td>m8</td><td>r/i8</td></tr>
      <tr><td>r16</td><td>r/m/i16</td></tr>
      <tr><td>m16</td><td>r/i16</td></tr>
      <tr><td>r32</td><td>r/m/i32</td></tr>
      <tr><td>m32</td><td>r/i32</td></tr>
      <tr><td rowspan=6>add</td><td rowspan=6>Add Integers</td><td>r8</td><td>r/m/i8</td><td rowspan=6>dest = dest + source</td></tr>
      <tr><td>m8</td><td>r/i8</td></tr>
      <tr><td>r16</td><td>r/m/i16</td></tr>
      <tr><td>m16</td><td>r/i16</td></tr>
      <tr><td>r32</td><td>r/m/i32</td></tr>
      <tr><td>m32</td><td>r/i32</td></tr>
      <tr><td rowspan=3>dec</td><td rowspan=3>Decrement Integer</td><td colspan=2>r/m8</td><td rowspan=3>operand = operand - 1</td></tr>
      <tr><td colspan=2>r/m16</td></tr>
      <tr><td colspan=2>r/m32</td></tr>
      <tr><td rowspan=3>div</td><td rowspan=3>Unsigned Integer Division</td><td colspan=2>r/m8</td><td>AH = AX % operand; AL = AX / operand</td></tr>
      <tr><td colspan=2>r/m16</td><td>DX = DX:AX % operand; AX= DX:AX / operand</td></tr>
      <tr><td colspan=2>r/m32</td><td>EDX = EDX:EAX % operand; EAX= EDX:EAX / operand</td>
      <tr><td rowspan=3>idiv</td><td rowspan=3>Signed Integer Division</td><td colspan=2>r/m8</td><td>AH = AX % operand; AL = AX / operand</td></tr>
      <tr><td colspan=2>r/m16</td><td>DX = DX:AX % operand; AX= DX:AX / operand</td></tr>
      <tr><td colspan=2>r/m32</td><td>EDX = EDX:EAX % operand; EAX= EDX:EAX / operand</td></tr>
      <tr><td rowspan=6>imul</td><td rowspan=6>Signed Integer Multiplication</td><td colspan=2>r/m8</td><td>AX = AL * operand</td></tr>
      <tr><td colspan=2>r/m16</td><td>DX:AX = AX * operand</td></tr>
      <tr><td colspan=2>r/m32</td><td>EDX:EAX = EAX * operand</td></tr>
      <tr><td>r8</td><td>r/m/i8</td><td rowspan=3>dest = dest * source</td></tr>
      <tr><td>r16</td><td>r/m/i16</td></tr>
      <tr><td>r32</td><td>r/m/i32</td></tr>
      <tr><td rowspan=3>inc</td><td rowspan=3>Increment Integer</td><td colspan=2>r/m8</td><td rowspan=3>operand = operand + 1</td></tr>
      <tr><td colspan=2>r/m16</td></tr>
      <tr><td colspan=2>r/m32</td></tr>
      <tr><td rowspan=3>mul</td><td rowspan=3>Unsigned Integer Multiplication</td><td colspan=2>r/m8</td><td>AX = AL * operand</td></tr>
      <tr><td colspan=2>r/m16</td><td>DX:AX = AX * operand</td></tr>
      <tr><td colspan=2>r/m32</td><td>EDX:EAX = EAX * operand</td></tr>
      <tr><td rowspan=3>neg</td><td rowspan=3>Negate Integer (2's Complement)</td><td colspan=2>r/m8</td><td rowspan=3>operand = -operand</td></tr>
      <tr><td colspan=2>r/m16</td></tr>
      <tr><td colspan=2>r/m32</td></tr>
      <tr><td rowspan=3>not</td><td rowspan=3>Invert Integer (1's Complement)</td><td colspan=2>r/m8</td><td rowspan=3>operand = -operand - 1</td></tr>
      <tr><td colspan=2>r/m16</td></tr>
      <tr><td colspan=2>r/m32</td></tr>
      <tr><td rowspan=6>ssb</td><td rowspan=6>Subtract Integers with Borrow (Carry)</td><td>r8</td><td>r/m/i8</td><td rowspan=6>dest = dest - source - carry</td></tr>
      <tr><td>m8</td><td>r/i8</td></tr>
      <tr><td>r16</td><td>r/m/i16</td></tr>
      <tr><td>m16</td><td>r/i16</td></tr>
      <tr><td>r32</td><td>r/m/i32</td></tr>
      <tr><td>m32</td><td>r/i32</td></tr>
      <tr><td rowspan=6>sub</td><td rowspan=6>Subtract Integers</td><td>r8</td><td>r/m/i8</td><td rowspan=6>dest = dest - source</td></tr>
      <tr><td>m8</td><td>r/i8</td></tr>
      <tr><td>r16</td><td>r/m/i16</td></tr>
      <tr><td>m16</td><td>r/i16</td></tr>
      <tr><td>r32</td><td>r/m/i32</td></tr>
      <tr><td>m32</td><td>r/i32</td></tr>
   </tbody>
</table>

