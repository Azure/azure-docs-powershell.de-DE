---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 3fdd6b407753e8edd9ba7faa074e287062f15fb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480261"
---
# <span data-ttu-id="fce93-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="fce93-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="fce93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fce93-102">SYNOPSIS</span></span>
<span data-ttu-id="fce93-103">Beendet die Sammlung von syslog-Daten von Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="fce93-103">Stops collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fce93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fce93-104">SYNTAX</span></span>

### <span data-ttu-id="fce93-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fce93-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fce93-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fce93-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fce93-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fce93-107">DESCRIPTION</span></span>
<span data-ttu-id="fce93-108">Das Cmdlet **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** beendet die Sammlung von syslog-Daten von verbundenen Linux-Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fce93-108">The **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="fce93-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fce93-109">EXAMPLES</span></span>

## <span data-ttu-id="fce93-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fce93-110">PARAMETERS</span></span>

### <span data-ttu-id="fce93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce93-111">-DefaultProfile</span></span>
<span data-ttu-id="fce93-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fce93-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fce93-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce93-113">-ResourceGroupName</span></span>
<span data-ttu-id="fce93-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="fce93-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="fce93-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="fce93-115">-Workspace</span></span>
<span data-ttu-id="fce93-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="fce93-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fce93-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fce93-117">-WorkspaceName</span></span>
<span data-ttu-id="fce93-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="fce93-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fce93-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fce93-119">-Confirm</span></span>
<span data-ttu-id="fce93-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fce93-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fce93-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce93-121">-WhatIf</span></span>
<span data-ttu-id="fce93-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fce93-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fce93-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fce93-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fce93-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce93-124">CommonParameters</span></span>
<span data-ttu-id="fce93-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce93-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce93-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce93-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce93-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fce93-127">INPUTS</span></span>

### <span data-ttu-id="fce93-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fce93-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="fce93-129">Parameter: Arbeitsbereich (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fce93-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="fce93-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fce93-130">System.String</span></span>

## <span data-ttu-id="fce93-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fce93-131">OUTPUTS</span></span>

### <span data-ttu-id="fce93-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fce93-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fce93-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fce93-133">NOTES</span></span>
* <span data-ttu-id="fce93-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="fce93-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fce93-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fce93-135">RELATED LINKS</span></span>

[<span data-ttu-id="fce93-136">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="fce93-136">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="fce93-137">Neu – AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="fce93-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


