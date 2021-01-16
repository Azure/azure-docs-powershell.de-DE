---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305851"
---
# Add-AzVMSecret

## SYNOPSIS
Fügt einem virtuellen Computer ein Geheimnis hinzu.

## SYNTAX

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzVMSecret"** fügt einem virtuellen Computer ein Geheimnis hinzu.
Mit diesem Wert können Sie dem virtuellen Computer ein Zertifikat hinzufügen.
Das Geheimnis muss in einem Schlüsseltresor gespeichert sein.
Weitere Informationen zum Schlüsseltresor finden Sie unter ["Was ist der Azure Key Vault?".](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)
Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](/powershell/module/az.keyvault) oder im [Set-AzKeyVaultSecret-Cmdlet.](/powershell/module/az.keyvault/set-azkeyvaultsecret)

## BEISPIELE

### Beispiel 1: Hinzufügen eines Geheimen zu einem virtuellen Computer
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Der erste Befehl erstellt ein Objekt des virtuellen Computers und speichert es dann in der $VirtualMachine Variable.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der zweite Befehl erstellt mithilfe des Cmdlets Get-Credential Anmeldeinformationen und speichert das Ergebnis dann in der $Credential Variable.
Der Befehl fordert Sie zur Eingabe eines Benutzernamens und Kennworts auf.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Credential` eingeben" aus.
Der dritte Befehl verwendet das **Cmdlet "Set-AzVMOperatingSystem",** um den virtuellen Computer zu konfigurieren, der in $VirtualMachine.
Der vierte Befehl weist der $SourceVaultId A0 eine Quelltresor-ID zur späteren Verwendung zu.
Bei dem Befehl wird davon ausgegangen, $SubscriptionId die Variable über einen geeigneten Wert verfügt.
Der fünfte Befehl weist der Variablen $CertificateStore 01 einen Wert zur späteren Verwendung zu.
Der sechste Befehl weist eine URL für einen Zertifikatspeicher zu.
Der siebte Befehl fügt dem virtuellen Computer, der in der Datei gespeichert ist, $VirtualMachine.
Der Parameter "SourceVaultId" gibt den Schlüsseltresor an.
Der Befehl gibt den Namen des Zertifikatspeichers und die URL des Zertifikats an.
Sie können **Add-AzVMSecret** wiederholt ausführen, um geheime Daten für andere Zertifikate hinzuzufügen.

## PARAMETERS

### -CertificateStore
Gibt den Namen eines Zertifikatspeichers auf dem virtuellen Computer an, auf dem das Betriebssystem Windows ausgeführt wird.
Dieses Cmdlet fügt dem speicher, den dieser Parameter angibt, das Zertifikat hinzu.
Sie können diesen Parameter nur für virtuelle Computer angeben, auf der das Betriebssystem Windows ausgeführt wird.

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
Gibt die URL an, die auf einen geheimen Schlüsseltresor verweist, der ein Zertifikat enthält.
Das Zertifikat ist die Base64-Codierung des folgenden JavaScript Object Notation (JSON)-Objekts, das in UTF-8 codiert ist: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", "password": " " } Derzeit akzeptiert dataType nur \<pfx-file-password\> PFX-Dateien.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Dies bedeutet, dass Sie denselben Wert für *"SourceVaultId"* verwenden können, wenn Sie mehrere Zertifikate aus demselben Schlüsseltresor hinzufügen.

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
Verwenden Sie das [Get-AzVM-Cmdlet,](./Get-AzVM.md) um ein Objekt des virtuellen Computers zu erhalten.
Sie können das [Cmdlet "New-AzVMConfig"](./New-AzVMConfig.md) verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
