---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178347"
---
# <span data-ttu-id="c6559-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="c6559-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="c6559-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6559-102">SYNOPSIS</span></span>
<span data-ttu-id="c6559-103">Exportiert den unformatierten Inhalt eines DSC-Berichts, der von einem DSC-Knoten an die Automatisierung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6559-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="c6559-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6559-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6559-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6559-105">DESCRIPTION</span></span>
<span data-ttu-id="c6559-106">Mit dem Cmdlet " **Export-AzAutomationDscNodeReportContent** " wird der unformatierte Inhalt eines APS-Berichts (Desired State Configuration, DSC) exportiert.</span><span class="sxs-lookup"><span data-stu-id="c6559-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="c6559-107">Ein DSC-Knoten sendet einen DSC-Bericht an die Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="c6559-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="c6559-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6559-108">EXAMPLES</span></span>

### <span data-ttu-id="c6559-109">Beispiel 1: Exportieren eines Berichts von einem DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="c6559-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="c6559-110">Dieser Satz von Befehlen exportiert den neuesten Bericht aus dem DSC-Knoten namens Computer14 auf den Desktop.</span><span class="sxs-lookup"><span data-stu-id="c6559-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="c6559-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6559-111">PARAMETERS</span></span>

### <span data-ttu-id="c6559-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c6559-112">-AutomationAccountName</span></span>
<span data-ttu-id="c6559-113">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="c6559-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="c6559-114">Dieses Cmdlet exportiert Berichtsinhalte für einen DSC-Knoten, der zum Automatisierungs Konto gehört, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c6559-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6559-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6559-115">-DefaultProfile</span></span>
<span data-ttu-id="c6559-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c6559-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6559-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c6559-117">-Force</span></span>
<span data-ttu-id="c6559-118">Gibt an, dass dieses Cmdlet eine vorhandene lokale Datei durch eine neue Datei ersetzt, die denselben Namen aufweist.</span><span class="sxs-lookup"><span data-stu-id="c6559-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="c6559-119">-Knoten-Nr</span><span class="sxs-lookup"><span data-stu-id="c6559-119">-NodeId</span></span>
<span data-ttu-id="c6559-120">Gibt die eindeutige ID des DSC-Knotens an, für den dieser Cmdlet Berichtsinhalte exportiert.</span><span class="sxs-lookup"><span data-stu-id="c6559-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6559-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="c6559-121">-OutputFolder</span></span>
<span data-ttu-id="c6559-122">Gibt den Ausgabeordner an, in dem dieses Cmdlet Berichtsinhalte exportiert.</span><span class="sxs-lookup"><span data-stu-id="c6559-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="c6559-123">-Berichts-Nr</span><span class="sxs-lookup"><span data-stu-id="c6559-123">-ReportId</span></span>
<span data-ttu-id="c6559-124">Gibt die eindeutige ID des vom Cmdlet exportierten DSC-Knoten Berichts an.</span><span class="sxs-lookup"><span data-stu-id="c6559-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6559-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6559-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6559-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c6559-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c6559-127">Dieses Cmdlet exportiert den Inhalt eines Berichts für den DSC-Knoten, der zu der Ressourcengruppe gehört, die von diesem Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c6559-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="c6559-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6559-128">-Confirm</span></span>
<span data-ttu-id="c6559-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6559-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6559-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6559-130">-WhatIf</span></span>
<span data-ttu-id="c6559-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6559-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6559-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6559-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6559-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6559-133">CommonParameters</span></span>
<span data-ttu-id="c6559-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6559-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6559-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6559-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6559-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6559-136">INPUTS</span></span>

### <span data-ttu-id="c6559-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c6559-137">System.Guid</span></span>

### <span data-ttu-id="c6559-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c6559-138">System.String</span></span>

## <span data-ttu-id="c6559-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6559-139">OUTPUTS</span></span>

### <span data-ttu-id="c6559-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="c6559-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="c6559-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6559-141">NOTES</span></span>

## <span data-ttu-id="c6559-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6559-142">RELATED LINKS</span></span>

[<span data-ttu-id="c6559-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="c6559-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="c6559-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c6559-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="c6559-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="c6559-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


