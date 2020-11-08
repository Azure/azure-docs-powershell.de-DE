---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: f60e254e9addf2e7052b010033d9c81ccc6a0a98
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010291"
---
# New-AzAutomationVariable

## Synopsis
Erstellt eine Automatisierungs Variable.

## Syntax

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzAutomationVariable** erstellt eine Variable in der Azure-Automatisierung.
Um die Variable zu verschlüsseln, geben Sie den *verschlüsselten* Parameter an.
Der verschlüsselte Zustand einer Variablen kann nach der Erstellung nicht geändert werden.

## Beispiele

### Beispiel 1: Erstellen einer Variablen mit einem einfachen Wert
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

Dieser Befehl erstellt eine Variable mit dem Namen StringVariable22 mit einem Zeichenfolgenwert im Automatisierungs Konto mit dem Namen Contoso17.

### Beispiel 2: Erstellen einer Variablen mit einem komplexen Wert
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

Der erste Befehl ruft einen virtuellen Computer mithilfe des Get-AzVM-Cmdlets ab.
Der Befehl speichert Sie in der $VirtualMachine-Variablen.
Der zweite Befehl erstellt eine Variable mit dem Namen ComplexVariable01 im Automatisierungs Konto mit dem Namen Contoso17.
Dieser Befehl verwendet ein komplexes Objekt für seinen Wert, in diesem Fall den virtuellen Computer in $VirtualMachine.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, in dem die Variable gespeichert werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Beschreibung
Gibt eine Beschreibung für die Variable an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verschlüsselt
Gibt an, ob dieses Cmdlet den Wert der Variablen für den Speicher verschlüsselt.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für die Variable an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, für die mit diesem Cmdlet eine Variable erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Gibt einen Wert für die Variable an.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Boolean

### System. Object

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. Variable

## Notizen

## Verwandte Links

[Get-AzAutomationVariable](./Get-AzAutomationVariable.md)

[Remove-AzAutomationVariable](./Remove-AzAutomationVariable.md)

[Satz-AzAutomationVariable](./Set-AzAutomationVariable.md)


