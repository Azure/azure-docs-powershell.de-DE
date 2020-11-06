---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: e6a77e8e89f710e1f8f827a27b1e1709ca8e3f1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479461"
---
# <span data-ttu-id="f6bbc-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="f6bbc-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="f6bbc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bbc-103">Beendet die Sammlung von Leistungsindikatoren auf Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-103">Stops collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6bbc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6bbc-104">SYNTAX</span></span>

### <span data-ttu-id="f6bbc-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6bbc-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6bbc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f6bbc-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6bbc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="f6bbc-108">Das Cmdlet **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** beendet die Sammlung von Leistungsindikatoren von verbundenen Linux-Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-108">The **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="f6bbc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6bbc-109">EXAMPLES</span></span>

## <span data-ttu-id="f6bbc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6bbc-110">PARAMETERS</span></span>

### <span data-ttu-id="f6bbc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6bbc-111">-DefaultProfile</span></span>
<span data-ttu-id="f6bbc-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f6bbc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6bbc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6bbc-113">-ResourceGroupName</span></span>
<span data-ttu-id="f6bbc-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="f6bbc-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="f6bbc-115">-Workspace</span></span>
<span data-ttu-id="f6bbc-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f6bbc-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f6bbc-117">-WorkspaceName</span></span>
<span data-ttu-id="f6bbc-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f6bbc-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6bbc-119">-Confirm</span></span>
<span data-ttu-id="f6bbc-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6bbc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6bbc-121">-WhatIf</span></span>
<span data-ttu-id="f6bbc-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6bbc-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6bbc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bbc-124">CommonParameters</span></span>
<span data-ttu-id="f6bbc-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6bbc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bbc-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6bbc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bbc-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6bbc-127">INPUTS</span></span>

### <span data-ttu-id="f6bbc-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f6bbc-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="f6bbc-129">Parameter: Arbeitsbereich (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f6bbc-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="f6bbc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f6bbc-130">System.String</span></span>

## <span data-ttu-id="f6bbc-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6bbc-131">OUTPUTS</span></span>

### <span data-ttu-id="f6bbc-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f6bbc-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f6bbc-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6bbc-133">NOTES</span></span>
* <span data-ttu-id="f6bbc-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="f6bbc-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f6bbc-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6bbc-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6bbc-136">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="f6bbc-136">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="f6bbc-137">Neu – AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="f6bbc-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


