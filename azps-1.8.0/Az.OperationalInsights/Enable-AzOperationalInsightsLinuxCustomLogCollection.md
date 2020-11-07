---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 67858083ed648e2965ea6fad2900ab63ef453901
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660071"
---
# <span data-ttu-id="d12af-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d12af-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="d12af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d12af-102">SYNOPSIS</span></span>
<span data-ttu-id="d12af-103">Startet eine Sammlung von benutzerdefinierten Protokollen von Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="d12af-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="d12af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d12af-104">SYNTAX</span></span>

### <span data-ttu-id="d12af-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d12af-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d12af-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d12af-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d12af-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d12af-107">DESCRIPTION</span></span>
<span data-ttu-id="d12af-108">Mit dem Cmdlet **enable-AzOperationalInsightsLinuxCustomLogCollection** wird eine Sammlung von benutzerdefinierten Protokollen von verbundenen Linux-Computern in einem Arbeitsbereich gestartet.</span><span class="sxs-lookup"><span data-stu-id="d12af-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d12af-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d12af-109">EXAMPLES</span></span>

## <span data-ttu-id="d12af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d12af-110">PARAMETERS</span></span>

### <span data-ttu-id="d12af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12af-111">-DefaultProfile</span></span>
<span data-ttu-id="d12af-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d12af-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d12af-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d12af-113">-ResourceGroupName</span></span>
<span data-ttu-id="d12af-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="d12af-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d12af-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="d12af-115">-Workspace</span></span>
<span data-ttu-id="d12af-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d12af-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d12af-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d12af-117">-WorkspaceName</span></span>
<span data-ttu-id="d12af-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d12af-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d12af-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d12af-119">-Confirm</span></span>
<span data-ttu-id="d12af-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d12af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d12af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d12af-121">-WhatIf</span></span>
<span data-ttu-id="d12af-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d12af-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d12af-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d12af-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d12af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12af-124">CommonParameters</span></span>
<span data-ttu-id="d12af-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12af-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d12af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12af-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d12af-127">INPUTS</span></span>

### <span data-ttu-id="d12af-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d12af-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d12af-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d12af-129">System.String</span></span>

## <span data-ttu-id="d12af-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d12af-130">OUTPUTS</span></span>

### <span data-ttu-id="d12af-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d12af-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d12af-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d12af-132">NOTES</span></span>
* <span data-ttu-id="d12af-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="d12af-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d12af-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d12af-134">RELATED LINKS</span></span>

[<span data-ttu-id="d12af-135">Deaktivieren-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d12af-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


