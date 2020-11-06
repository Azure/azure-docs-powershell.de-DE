---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 99ec8caac4a4e5d2dfab6b881bb32eee62a90371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496346"
---
# <span data-ttu-id="08db5-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="08db5-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="08db5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08db5-102">SYNOPSIS</span></span>
<span data-ttu-id="08db5-103">Startet die Sammlung von Leistungsindikatoren auf Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="08db5-103">Starts collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08db5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08db5-104">SYNTAX</span></span>

### <span data-ttu-id="08db5-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="08db5-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08db5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="08db5-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08db5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08db5-107">DESCRIPTION</span></span>
<span data-ttu-id="08db5-108">Mit dem Cmdlet **enable-AzureRmOperationalInsightsLinuxPerformanceCollection** wird die Sammlung von Leistungsindikatoren von verbundenen Linux-Computern in einem Arbeitsbereich gestartet.</span><span class="sxs-lookup"><span data-stu-id="08db5-108">The **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="08db5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08db5-109">EXAMPLES</span></span>

## <span data-ttu-id="08db5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="08db5-110">PARAMETERS</span></span>

### <span data-ttu-id="08db5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08db5-111">-DefaultProfile</span></span>
<span data-ttu-id="08db5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="08db5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08db5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08db5-113">-ResourceGroupName</span></span>
<span data-ttu-id="08db5-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="08db5-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="08db5-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="08db5-115">-Workspace</span></span>
<span data-ttu-id="08db5-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="08db5-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="08db5-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08db5-117">-WorkspaceName</span></span>
<span data-ttu-id="08db5-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="08db5-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="08db5-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08db5-119">-Confirm</span></span>
<span data-ttu-id="08db5-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08db5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08db5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08db5-121">-WhatIf</span></span>
<span data-ttu-id="08db5-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08db5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08db5-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08db5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08db5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08db5-124">CommonParameters</span></span>
<span data-ttu-id="08db5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08db5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08db5-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08db5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08db5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08db5-127">INPUTS</span></span>

### <span data-ttu-id="08db5-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="08db5-128">PSWorkspace</span></span>
<span data-ttu-id="08db5-129">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="08db5-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="08db5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08db5-130">OUTPUTS</span></span>

### <span data-ttu-id="08db5-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="08db5-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="08db5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="08db5-132">NOTES</span></span>
* <span data-ttu-id="08db5-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="08db5-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="08db5-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08db5-134">RELATED LINKS</span></span>

[<span data-ttu-id="08db5-135">Deaktivieren-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="08db5-135">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


