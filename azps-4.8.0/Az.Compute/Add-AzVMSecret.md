---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395338"
---
# Add-AzVMSecret

## Synopsis
Fügt einen geheimen Schlüssel zu einem virtuellen Computer hinzu.

## Syntax

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzVMSecret** fügt einem virtuellen Computer einen Schlüssel hinzu.
Mit diesem Wert können Sie dem virtuellen Computer ein Zertifikat hinzufügen.
Das Kennwort muss in einem schlüsseltresor gespeichert werden.
Weitere Informationen zu Key Vault finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](/powershell/module/az.keyvault) oder dem Cmdlet " [AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) ".

## Beispiele

### Beispiel 1: Hinzufügen eines Geheimnisses zu einem virtuellen Computer
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der zweite Befehl erstellt ein Anmeldeinformationsobjekt mithilfe des Get-Credential-Cmdlets und speichert dann das Ergebnis in der $Credential-Variablen.
Der Befehl fordert Sie auf, einen Benutzernamen und ein Kennwort einzugeben.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .
Der dritte Befehl verwendet das Cmdlet " **Satz-AzVMOperatingSystem** ", um den in $VirtualMachine gespeicherten virtuellen Computer zu konfigurieren.
Der vierte Befehl weist der $SourceVaultId Variablen eine Quell Tresor-ID zur späteren Verwendung zu.
Der Befehl geht davon aus, dass die $SubscriptionId Variable über einen geeigneten Wert verfügt.
Der fünfte Befehl weist der $CertificateStore 01-Variablen einen Wert für die spätere Verwendung zu.
Der sechste Befehl weist eine URL für einen Zertifikatspeicher zu.
Der siebte Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, einen Schlüssel hinzu.
Der SourceVaultId-Parameter gibt den schlüsseltresor an.
Der Befehl gibt den Namen des Zertifikatspeichers und die URL des Zertifikats an.
Sie können das **Add-AzVMSecret** wiederholt ausführen, um Geheimnisse für andere Zertifikate hinzuzufügen.

## Parameter

### -CertificateStore
Gibt den Namen eines Zertifikatspeichers auf dem virtuellen Computer an, auf dem das Windows-Betriebssystem ausgeführt wird.
Mit diesem Cmdlet wird das Zertifikat dem Store hinzugefügt, das dieser Parameter angibt.
Sie können diesen Parameter nur für virtuelle Computer angeben, auf denen das Windows-Betriebssystem ausgeführt wird.

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
Gibt die URL an, die auf ein schlüsseltresor-Kennwort verweist, das ein Zertifikat enthält.
Bei dem Zertifikat handelt es sich um die Base64-Codierung des folgenden JSON-Objekts (JavaScript Object Notation), das in UTF-8 codiert ist: {"Daten": " \<Base64-encoded-file\> ", "Datentyp": " \<file-format\> ", "Kennwort": " \<pfx-file-password\> "} der Datentyp akzeptiert derzeit nur PFX-Dateien.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
Gibt die Ressourcen-ID des Schlüsseldepots an, das die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.
Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.
Das bedeutet, dass Sie für *SourceVaultId* denselben Wert verwenden können, wenn Sie mehrere Zertifikate aus demselben schlüsseltresor hinzufügen.

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
Verwenden Sie das Cmdlet [Get-AzVM](./Get-AzVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.
Sie können das Cmdlet [New-AzVMConfig](./New-AzVMConfig.md) verwenden, um ein Objekt eines virtuellen Computers zu erstellen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Notizen

## Verwandte Links

[Get-AzVM](./Get-AzVM.md)

[Neu – AzVMConfig](./New-AzVMConfig.md)

[Satz-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
