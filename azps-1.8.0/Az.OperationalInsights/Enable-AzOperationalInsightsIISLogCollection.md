---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 75b037903adf52b1ba1407ff40e2bfbb610a6dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660072"
---
# <span data-ttu-id="a151a-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="a151a-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="a151a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a151a-102">SYNOPSIS</span></span>
<span data-ttu-id="a151a-103">Startet die Sammlung von IIS-Protokollen von Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a151a-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="a151a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a151a-104">SYNTAX</span></span>

### <span data-ttu-id="a151a-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a151a-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a151a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a151a-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a151a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a151a-107">DESCRIPTION</span></span>
<span data-ttu-id="a151a-108">Das Cmdlet **enable-AzOperationalInsightsIISLogCollection** startet die Sammlung von Internet Informationsdienste (IIS)-Protokollen von verbundenen Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a151a-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="a151a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a151a-109">EXAMPLES</span></span>

## <span data-ttu-id="a151a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a151a-110">PARAMETERS</span></span>

### <span data-ttu-id="a151a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a151a-111">-DefaultProfile</span></span>
<span data-ttu-id="a151a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a151a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a151a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a151a-113">-ResourceGroupName</span></span>
<span data-ttu-id="a151a-114">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="a151a-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="a151a-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a151a-115">-Workspace</span></span>
<span data-ttu-id="a151a-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a151a-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a151a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a151a-117">-WorkspaceName</span></span>
<span data-ttu-id="a151a-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a151a-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a151a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a151a-119">-Confirm</span></span>
<span data-ttu-id="a151a-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a151a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a151a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a151a-121">-WhatIf</span></span>
<span data-ttu-id="a151a-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a151a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a151a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a151a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a151a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a151a-124">CommonParameters</span></span>
<span data-ttu-id="a151a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a151a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a151a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a151a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a151a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a151a-127">INPUTS</span></span>

### <span data-ttu-id="a151a-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a151a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a151a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a151a-129">System.String</span></span>

## <span data-ttu-id="a151a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a151a-130">OUTPUTS</span></span>

### <span data-ttu-id="a151a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a151a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a151a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a151a-132">NOTES</span></span>

## <span data-ttu-id="a151a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a151a-133">RELATED LINKS</span></span>

[<span data-ttu-id="a151a-134">Deaktivieren-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="a151a-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


