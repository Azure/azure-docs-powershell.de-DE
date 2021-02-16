---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147977"
---
# Remove-AzDnsZone

## SYNOPSIS
Entfernt eine DNS-Zone aus einer Ressourcengruppe.

## SYNTAX

### Felder
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Remove-AzDnsZone"** löscht eine Domain Name System (DNS)-Zone dauerhaft aus einer angegebenen Ressourcengruppe.
Alle in der Zone enthaltenen Datensatzsätze werden ebenfalls gelöscht.
Sie können ein **DnsZone-Objekt** mit dem *Parameter "Name"* oder mit dem Pipelineoperator übergeben, oder Sie können die *Parameter "ZoneName"* und *"ResourceGroupName"* angeben.
Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.
Wenn Sie die Zone mithilfe eines (über die  Pipeline oder den Zonenparameter übergebenen) **DnsZone-Objekts** angeben, wird die Zone nicht gelöscht, wenn sie seit dem Abrufen des lokalen **"DnsZone"-Objekts** in Azure DNS geändert wurde (nur Vorgänge direkt für die DNS-Zonenressourcen zählen als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht).
Dies bietet Schutz für Änderungen gleichzeitiger Zonen.
Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.

## BEISPIELE

### Beispiel 1: Entfernen einer Zone
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Mit diesem Befehl wird die Zone namens "myzone.com" aus der Ressourcengruppe "MyResourceGroup" entfernt.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Name
Gibt den Namen der DNS-Zone an, die von diesem Cmdlet entfernt wird.
Sie müssen auch den Parameter *"ResourceGroupName"* angeben.
Alternativ können Sie die DNS-Zone mit dem Parameter *"Zone"* angeben.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Wenn Sie die Zone mithilfe eines (über die  Pipeline oder den Zonenparameter übergebenen) **DnsZone-Objekts** angeben, wird die Zone nicht gelöscht, wenn sie seit dem Abrufen des lokalen **"DnsZone"-Objekts** in Azure DNS geändert wurde (nur Vorgänge direkt für die DNS-Zonenressourcen zählen als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht).
Dies bietet Schutz für Änderungen gleichzeitiger Zonen.
Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die die zu entfernende Zone enthält.
Sie müssen auch den *Parameter "ZoneName"* angeben.
Alternativ können Sie die DNS-Zone mit einem **DnsZone-Objekt** angeben, das entweder über die Pipeline oder den Parameter *"Zone" übergeben* wird.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Gibt die zu löschende DNS-Zone an.
Das **übergebene "DnsZone"-Objekt** kann auch über die Pipeline übergeben werden.
Alternativ können Sie die zu löschende DNS-Zone mit den *Parametern "ZoneName"* und *"ResourceGroupName"* angeben.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

## AUSGABEN

### System.Boolean

## HINWEISE
Aufgrund der potenziell hohen Auswirkungen des Löschens einer DNS-Zone fordert dieses Cmdlet standardmäßig zur Bestätigung auf, wenn die variable $ConfirmPreference Windows PowerShell einen anderen Wert als "None" hat.
Wenn Sie *"Bestätigen"* oder *"Bestätigen:$True"* angeben, fordert Sie dieses Cmdlet zur Bestätigung auf, bevor es ausgeführt wird.
Wenn Sie *"Confirm:$False" angeben,* werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert. 

## LINKS ZU VERWANDTEN THEMEN

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
