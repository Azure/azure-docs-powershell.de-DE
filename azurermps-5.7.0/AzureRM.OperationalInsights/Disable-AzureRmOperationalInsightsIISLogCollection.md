---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 44f5ffd63f2bb89f2e26d8ded6a0c7f64181bf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665179"
---
# <span data-ttu-id="972ab-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="972ab-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="972ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="972ab-102">SYNOPSIS</span></span>
<span data-ttu-id="972ab-103">Beendet die Sammlung von IIS-Protokollen von Computern.</span><span class="sxs-lookup"><span data-stu-id="972ab-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="972ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="972ab-104">SYNTAX</span></span>

### <span data-ttu-id="972ab-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="972ab-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ab-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="972ab-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="972ab-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="972ab-107">DESCRIPTION</span></span>
<span data-ttu-id="972ab-108">Das Cmdlet **Disable-AzureRmOperationalInsightsIISLogCollection** beendet die Sammlung von Internet Informationsdienste-Protokollen (IIS) von verbundenen Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="972ab-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="972ab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="972ab-109">EXAMPLES</span></span>

## <span data-ttu-id="972ab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="972ab-110">PARAMETERS</span></span>

### <span data-ttu-id="972ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972ab-111">-DefaultProfile</span></span>
<span data-ttu-id="972ab-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="972ab-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972ab-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972ab-113">-ResourceGroupName</span></span>
<span data-ttu-id="972ab-114">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="972ab-114">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="972ab-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="972ab-115">-Workspace</span></span>
<span data-ttu-id="972ab-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="972ab-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="972ab-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="972ab-117">-WorkspaceName</span></span>
<span data-ttu-id="972ab-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="972ab-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="972ab-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="972ab-119">-Confirm</span></span>
<span data-ttu-id="972ab-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="972ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="972ab-121">-WhatIf</span></span>
<span data-ttu-id="972ab-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="972ab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="972ab-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="972ab-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972ab-124">CommonParameters</span></span>
<span data-ttu-id="972ab-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="972ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972ab-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="972ab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972ab-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="972ab-127">INPUTS</span></span>

### <span data-ttu-id="972ab-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="972ab-128">PSWorkspace</span></span>
<span data-ttu-id="972ab-129">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="972ab-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="972ab-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="972ab-130">OUTPUTS</span></span>

### <span data-ttu-id="972ab-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="972ab-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="972ab-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="972ab-132">NOTES</span></span>
* <span data-ttu-id="972ab-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="972ab-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="972ab-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="972ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="972ab-135">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="972ab-135">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


