---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 92fbc7e67bb81422e021a23810f3045b5cf32cba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166197"
---
# <span data-ttu-id="e6176-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e6176-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="e6176-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6176-102">SYNOPSIS</span></span>
<span data-ttu-id="e6176-103">Beendet die Sammlung von Leistungsindikatoren auf Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="e6176-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="e6176-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6176-104">SYNTAX</span></span>

### <span data-ttu-id="e6176-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6176-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6176-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e6176-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6176-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6176-107">DESCRIPTION</span></span>
<span data-ttu-id="e6176-108">Das Cmdlet **Disable-AzOperationalInsightsLinuxPerformanceCollection** beendet die Sammlung von Leistungsindikatoren von verbundenen Linux-Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="e6176-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="e6176-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6176-109">EXAMPLES</span></span>

## <span data-ttu-id="e6176-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6176-110">PARAMETERS</span></span>

### <span data-ttu-id="e6176-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6176-111">-DefaultProfile</span></span>
<span data-ttu-id="e6176-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e6176-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6176-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6176-113">-ResourceGroupName</span></span>
<span data-ttu-id="e6176-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="e6176-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6176-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="e6176-115">-Workspace</span></span>
<span data-ttu-id="e6176-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e6176-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6176-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6176-117">-WorkspaceName</span></span>
<span data-ttu-id="e6176-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e6176-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6176-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6176-119">-Confirm</span></span>
<span data-ttu-id="e6176-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6176-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6176-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6176-121">-WhatIf</span></span>
<span data-ttu-id="e6176-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6176-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6176-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6176-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6176-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6176-124">CommonParameters</span></span>
<span data-ttu-id="e6176-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6176-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6176-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6176-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6176-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6176-127">INPUTS</span></span>

### <span data-ttu-id="e6176-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6176-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e6176-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e6176-129">System.String</span></span>

## <span data-ttu-id="e6176-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6176-130">OUTPUTS</span></span>

### <span data-ttu-id="e6176-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e6176-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e6176-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6176-132">NOTES</span></span>
* <span data-ttu-id="e6176-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="e6176-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e6176-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6176-134">RELATED LINKS</span></span>

[<span data-ttu-id="e6176-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e6176-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="e6176-136">Neu – AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="e6176-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


