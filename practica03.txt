<?php

$cantidad1 = $_POST['cantidad1'];
$producto1 = $_POST['producto1'];
$precio1 = $_POST['precio1'];
$tota1 = $cantidad1 * $precio1;

$cantidad2 = $_POST['cantidad2'];
$producto2 = $_POST['producto2'];
$precio2 = $_POST['precio2'];
$tota2 = $cantidad2 * $precio2;


$cantidad3 = $_POST['cantidad3'];
$producto3 = $_POST['producto3'];
$precio3 = $_POST['precio3'];
$tota3 = $cantidad3 * $precio3;

?>

<html>
	<body>
		<p>
			<fieldset>
				<legend> Productos Vendidos </legend>
				<br>

				<table>
					<tr>
						<th> Cantidad </th>
						<th> Producto </th>
						<th> Precio U </th>
                        <th> Total </th>
					</tr>
                    

					<tr>
						<td> <?php echo $cantidad1; ?> </td>
						<td> <?php echo $producto1; ?> </td>
						<td> <?php echo $precio1; ?> </td>
                        <td> <?php echo $tota1; ?> </td>
					</tr>

					<tr>
						<td> <?php echo $cantidad2; ?> </td>
						<td> <?php echo $producto2; ?> </td>
						<td> <?php echo $precio2; ?> </td>
                        <td> <?php echo $tota2; ?> </td>
					</tr>

					<tr>
						<td> <?php echo $cantidad3; ?></td>
						<td> <?php echo $producto3; ?> </td>
						<td> <?php echo $precio3; ?> </td>
                        <td> <?php echo $tota3; ?> </td>
					</tr>
				</table>
			<?php

			$suma = (($cantidad1 * $precio1) + ($cantidad2 * $precio2) + ($cantidad3 * $precio3));
			$iva = $suma * .16;
			$total = $suma + $iva;
		
			?>

			<p>
				Subtotal : <?php echo $suma; ?>
				<br>
				IVA :  <?php echo $iva; ?>
				<br>
				Total : <?php echo $total; ?>
				<br>
			</p>

			</fieldset>
		</p>
	</body>
</html>