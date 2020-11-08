---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: f5bc73ee6fc2f3c20b92f8780bcddec99bc46fee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174944"
---
# <span data-ttu-id="9d444-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9d444-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="9d444-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d444-102">SYNOPSIS</span></span>
<span data-ttu-id="9d444-103">Beendet die Sammlung von syslog-Daten von Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="9d444-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="9d444-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d444-104">SYNTAX</span></span>

### <span data-ttu-id="9d444-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d444-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d444-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9d444-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d444-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d444-107">DESCRIPTION</span></span>
<span data-ttu-id="9d444-108">Das Cmdlet **Disable-AzOperationalInsightsLinuxSyslogCollection** beendet die Sammlung von syslog-Daten von verbundenen Linux-Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="9d444-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="9d444-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d444-109">EXAMPLES</span></span>

## <span data-ttu-id="9d444-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d444-110">PARAMETERS</span></span>

### <span data-ttu-id="9d444-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d444-111">-DefaultProfile</span></span>
<span data-ttu-id="9d444-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9d444-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d444-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d444-113">-ResourceGroupName</span></span>
<span data-ttu-id="9d444-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="9d444-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="9d444-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="9d444-115">-Workspace</span></span>
<span data-ttu-id="9d444-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9d444-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9d444-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9d444-117">-WorkspaceName</span></span>
<span data-ttu-id="9d444-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9d444-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9d444-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9d444-119">-Confirm</span></span>
<span data-ttu-id="9d444-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d444-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d444-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d444-121">-WhatIf</span></span>
<span data-ttu-id="9d444-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d444-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d444-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d444-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d444-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d444-124">CommonParameters</span></span>
<span data-ttu-id="9d444-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d444-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d444-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d444-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d444-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d444-127">INPUTS</span></span>

### <span data-ttu-id="9d444-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9d444-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9d444-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9d444-129">System.String</span></span>

## <span data-ttu-id="9d444-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d444-130">OUTPUTS</span></span>

### <span data-ttu-id="9d444-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9d444-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9d444-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d444-132">NOTES</span></span>
* <span data-ttu-id="9d444-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="9d444-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9d444-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d444-134">RELATED LINKS</span></span>

[<span data-ttu-id="9d444-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9d444-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="9d444-136">Neu – AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="9d444-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


