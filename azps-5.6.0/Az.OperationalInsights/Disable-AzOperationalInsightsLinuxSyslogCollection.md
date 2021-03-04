---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 7593ad23952b9920fdd7e7fa9d75e22e9fe65059
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942360"
---
# <span data-ttu-id="a9640-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="a9640-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="a9640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9640-102">SYNOPSIS</span></span>
<span data-ttu-id="a9640-103">Beendet die Sammlung von Syslogdaten von Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="a9640-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="a9640-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9640-104">SYNTAX</span></span>

### <span data-ttu-id="a9640-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9640-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9640-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a9640-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9640-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9640-107">DESCRIPTION</span></span>
<span data-ttu-id="a9640-108">Das **Cmdlet Disable-AzOperationalInsightsLinuxSyslogCollection** beendet die Sammlung von Syslogdaten von verbundenen Linux-Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a9640-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="a9640-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9640-109">EXAMPLES</span></span>

## <span data-ttu-id="a9640-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a9640-110">PARAMETERS</span></span>

### <span data-ttu-id="a9640-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9640-111">-DefaultProfile</span></span>
<span data-ttu-id="a9640-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a9640-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9640-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9640-113">-ResourceGroupName</span></span>
<span data-ttu-id="a9640-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="a9640-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="a9640-115">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a9640-115">-Workspace</span></span>
<span data-ttu-id="a9640-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9640-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a9640-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9640-117">-WorkspaceName</span></span>
<span data-ttu-id="a9640-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9640-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a9640-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9640-119">-Confirm</span></span>
<span data-ttu-id="a9640-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9640-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9640-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9640-121">-WhatIf</span></span>
<span data-ttu-id="a9640-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9640-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9640-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9640-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9640-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9640-124">CommonParameters</span></span>
<span data-ttu-id="a9640-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9640-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9640-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9640-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9640-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9640-127">INPUTS</span></span>

### <span data-ttu-id="a9640-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a9640-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a9640-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a9640-129">System.String</span></span>

## <span data-ttu-id="a9640-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9640-130">OUTPUTS</span></span>

### <span data-ttu-id="a9640-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a9640-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a9640-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a9640-132">NOTES</span></span>
* <span data-ttu-id="a9640-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="a9640-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a9640-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a9640-134">RELATED LINKS</span></span>

[<span data-ttu-id="a9640-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="a9640-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="a9640-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="a9640-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


