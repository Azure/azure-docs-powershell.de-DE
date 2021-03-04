---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: c4eef22d2bf188d56c0d7af66fb42ad3bce7b5be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923848"
---
# Add-AzVMSecret

## SYNOPSIS
Fügt einem virtuellen Computer einen Geheimtipp hinzu.

## SYNTAX

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Add-AzVMSecret-Cmdlet** fügt einem virtuellen Computer einen Geheimtipp hinzu.
Mit diesem Wert können Sie dem virtuellen Computer ein Zertifikat hinzufügen.
Der Geheimschlüssel muss in einem Schlüsseltresor gespeichert sein.
Weitere Informationen zum Schlüsseltresor finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) oder das [Set-AzKeyVaultSecret-Cmdlet.](/powershell/module/az.keyvault/set-azkeyvaultsecret)

## BEISPIELE

### Beispiel 1: Hinzufügen eines Geheimtipps zu einem virtuellen Computer
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Mit dem ersten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der zweite Befehl erstellt ein Anmeldeinformationsobjekt mithilfe des cmdlets Get-Credential und speichert dann das Ergebnis in $Credential Variablen.
Mit dem Befehl werden Sie aufgefordert, einen Benutzernamen und ein Kennwort einzugeben.
Weitere Informationen finden Sie unter `Get-Help Get-Credential` .
Der dritte Befehl verwendet das **Cmdlet Set-AzVMOperatingSystem,** um den virtuellen Computer zu konfigurieren, der auf einem $VirtualMachine.
Der vierte Befehl weist der $SourceVaultId-Variable eine Quelltresor-ID für die spätere Verwendung zu.
Der Befehl geht davon aus, dass die $SubscriptionId einen geeigneten Wert hat.
Der fünfte Befehl weist der Variablen $CertificateStore 01 einen Wert für die spätere Verwendung zu.
Der sechste Befehl weist eine URL für einen Zertifikatspeicher zu.
Mit dem siebten Befehl wird dem virtuellen Computer, der auf dem Computer gespeichert ist, ein $VirtualMachine.
Der Parameter SourceVaultId gibt den Schlüsseltresor an.
Der Befehl gibt den Namen des Zertifikatspeichers und die URL des Zertifikats an.
Sie können das **Add-AzVMSecret** wiederholt ausführen, um Geheimnisse für andere Zertifikate hinzuzufügen.

## PARAMETER

### -CertificateStore
Gibt den Namen eines Zertifikatspeichers auf dem virtuellen Computer an, auf dem das Windows-Betriebssystem ausgeführt wird.
Dieses Cmdlet fügt das Zertifikat dem Speicher hinzu, den dieser Parameter angibt.
Sie können diesen Parameter nur für virtuelle Computer angeben, auf den das Windows-Betriebssystem ausgeführt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Gibt die URL an, die auf einen Schlüsseltresorschlüssel verweist, der ein Zertifikat enthält.
Das Zertifikat ist die Base64-Codierung des folgenden JavaScript Object Notation (JSON)-Objekts, das in UTF-8 codiert ist: { "data": " \<Base64-encoded-file\> ", "dataType": " ", "password": " " } Zurzeit akzeptiert dataType nur \<file-format\> \<pfx-file-password\> PFX-Dateien.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceVaultId
Gibt die Ressourcen-ID des Schlüsseltresor an, der die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.
Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.
Dies bedeutet, dass Sie denselben Wert für *SourceVaultId* verwenden können, wenn Sie mehrere Zertifikate aus demselben Schlüsseltresor hinzufügen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.
Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie [das Get-AzVM-Cmdlet.](./Get-AzVM.md)
Sie können das [Cmdlet New-AzVMConfig](./New-AzVMConfig.md) verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
