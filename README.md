# Random
sgBox(0, "", _Random(-1)) ; Example  Func _Random($nNum1 = 0, $nNum2 = 0, $iFlag = 0)     If Not IsNumber($nNum1) Then Return SetError(1, 0, 0) ; Invalid 1st parameter     Switch @NumParams         Case 0             Return Random()         Case 1             If $nNum1 &lt; 0 Then Return -Random(-$nNum1)             Return Random($nNum1)         Case Else             If Not IsNumber($nNum1) Or ($iFlag &lt;> 0 And $iFlag &lt;> 1) Then Return SetError(2, 0, 0) ; Invalid 2nd or 3rd parameter             If $nNum1 = $nNum2 Then Return $nNum1             If $nNum2 > $nNum1 Then Return Random($nNum1, $nNum2, $iFlag)             Return Random($nNum2, $nNum1, $iFlag)     EndSwitch EndFunc
