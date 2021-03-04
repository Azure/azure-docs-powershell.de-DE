---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 294669fe5b9e5aeb01dfbfa7ab538a0f6d411cca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949619"
---
# Get-AzBatchTaskCount

## SYNOPSIS
Ruft die Anzahl der Aufgaben für den angegebenen Auftrag ab.

## SYNTAX

### ID
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Get-AzBatchTaskCount** ruft die Azure Batch-Aufgabenanzahl für einen Batchauftrag ab.
Geben Sie einen Auftrag entweder über den *Parameter "JobId"* oder den *Parameter "Auftrag"* an.
Vorgangszählungen stellen eine Anzahl der Vorgänge nach aktivem, ausgeführten oder abgeschlossenen Vorgangszustand und eine Anzahl von Vorgängen, die erfolgreich oder fehlgeschlagen sind, zur Verfügung. Aufgaben im Vorbereitungszustand werden als ausgeführt gezählt. Wenn der Gültigkeitsprüfungsstatus nicht mehr validiert ist, konnte der Batchdienst die Statuszählungen nicht mit den Vorgangszuständen überprüfen, wie in der LISTENaufgaben-API gemeldet. Der Gültigkeitsprüfungsstatus ist möglicherweise nicht mehr aktiviert, wenn der Auftrag mehr als 200.000 Vorgänge enthält.

## BEISPIELE

### Beispiel 1: Erhalten von Aufgabenanzahlen nach ID
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Mit diesem Befehl werden die Aufgabenanzahlen für "Auftrag01" ermittelt.
Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.

## PARAMETER

### -BatchContext
Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batchdienst verwendet werden soll.
Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.
Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.
Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.
Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Job
Gibt den Auftrag an, der Aufgaben enthält, die dieses Cmdlet erhält.
Um ein **PSCloudJob-Objekt** zu erhalten, verwenden Sie das Get-AzBatchJob Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Die ID des Auftrags, für den aufgabenanzahlt werden soll.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Batch. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## AUSGABEN

### Microsoft.Azure.Commands.Batch. Models.PSTaskCounts

## NOTIZEN

## VERWANDTE LINKS

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Azure Batch-Cmdlets](/powershell/module/Az.Batch/)
