---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 2a007a2695141d0772afeb025644f8a3dbf4efb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942323"
---
# <span data-ttu-id="0ccb1-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="0ccb1-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="0ccb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ccb1-102">SYNOPSIS</span></span>
<span data-ttu-id="0ccb1-103">Startet die Sammlung von Syslogdaten von Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="0ccb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ccb1-104">SYNTAX</span></span>

### <span data-ttu-id="0ccb1-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ccb1-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ccb1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0ccb1-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ccb1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ccb1-107">DESCRIPTION</span></span>
<span data-ttu-id="0ccb1-108">Das **Cmdlet Enable-AzOperationalInsightsLinuxSyslogCollection** startet die Sammlung von Syslogdaten von verbundenen Linux-Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="0ccb1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ccb1-109">EXAMPLES</span></span>

## <span data-ttu-id="0ccb1-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0ccb1-110">PARAMETERS</span></span>

### <span data-ttu-id="0ccb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ccb1-111">-DefaultProfile</span></span>
<span data-ttu-id="0ccb1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0ccb1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ccb1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ccb1-113">-ResourceGroupName</span></span>
<span data-ttu-id="0ccb1-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="0ccb1-115">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="0ccb1-115">-Workspace</span></span>
<span data-ttu-id="0ccb1-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0ccb1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0ccb1-117">-WorkspaceName</span></span>
<span data-ttu-id="0ccb1-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0ccb1-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ccb1-119">-Confirm</span></span>
<span data-ttu-id="0ccb1-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ccb1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ccb1-121">-WhatIf</span></span>
<span data-ttu-id="0ccb1-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ccb1-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ccb1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ccb1-124">CommonParameters</span></span>
<span data-ttu-id="0ccb1-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ccb1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ccb1-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ccb1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ccb1-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ccb1-127">INPUTS</span></span>

### <span data-ttu-id="0ccb1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0ccb1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="0ccb1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0ccb1-129">System.String</span></span>

## <span data-ttu-id="0ccb1-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ccb1-130">OUTPUTS</span></span>

### <span data-ttu-id="0ccb1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0ccb1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0ccb1-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0ccb1-132">NOTES</span></span>
* <span data-ttu-id="0ccb1-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="0ccb1-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0ccb1-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0ccb1-134">RELATED LINKS</span></span>

[<span data-ttu-id="0ccb1-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="0ccb1-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="0ccb1-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="0ccb1-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


