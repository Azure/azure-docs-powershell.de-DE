---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 2ec50d8e0c11143f72e327a7b73784c1a49e926c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938912"
---
# Add-AzVMAdditionalUnattendContent

## SYNOPSIS
Fügt der unbeaufsichtigten Windows Setup-Antwortdatei Informationen hinzu.

## SYNTAX

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Add-AzVMAdditionalUnattendContent** fügt der unbeaufsichtigten Windows Setup-Antwortdatei Informationen hinzu.
Geben Sie zusätzliche xml-formatierte Basisinformationen an, die von diesem Cmdlet zur unattend.xml werden.

## BEISPIELE

### Beispiel 1: Hinzufügen von Inhalt zu unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Der erste Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.
Mit dem zweiten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.
Der dritte Befehl erstellt ein Anmeldeinformationsobjekt mithilfe des cmdlets Get-Credential und speichert dann das Ergebnis in der $Credential Variablen.
Mit dem Befehl werden Sie aufgefordert, einen Benutzernamen und ein Kennwort einzugeben.
Weitere Informationen finden Sie unter `Get-Help Get-Credential` .
Der vierte Befehl verwendet das **Set-AzVMOperatingSystem-Cmdlet,** um den virtuellen Computer zu konfigurieren, der auf einem $VirtualMachine.
Der fünfte Befehl weist der Variablen inhalt $AucContent zu.
Der Inhalt enthält ein Kennwort.
Der letzte Befehl fügt den in der Datei gespeicherten $AucContent der datei unattend.xml hinzu.

## PARAMETER

### -Inhalt
Gibt basis-64-codierten XML-formatierten Inhalt an.
Dieses Cmdlet fügt den Inhalt der datei unattend.xml hinzu.
Der XML-Inhalt muss kleiner als 4 KB sein und das Stammelement für die Einstellung oder das Feature enthalten, das von diesem Cmdlet eingefügt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### -SettingName
Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.
Die zulässigen Werte für diesen Parameter sind:
- FirstLogonCommands
- AutoLogon

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.
Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie [das Get-AzVM-Cmdlet.](./Get-AzVM.md)
Erstellen Sie ein Objekt eines virtuellen Computers mithilfe des [Cmdlets New-AzVMConfig.](./New-AzVMConfig.md)

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

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTIZEN

## VERWANDTE LINKS

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzVMConfig](./New-AzVMConfig.md)
