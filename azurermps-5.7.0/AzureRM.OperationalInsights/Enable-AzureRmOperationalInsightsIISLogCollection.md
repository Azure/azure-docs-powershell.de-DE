---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 417bc080d707c3da02dd8a0083fb707f79d0a999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496353"
---
# <span data-ttu-id="e44e1-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="e44e1-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="e44e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e44e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e44e1-103">Startet die Sammlung von IIS-Protokollen von Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="e44e1-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e44e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e44e1-104">SYNTAX</span></span>

### <span data-ttu-id="e44e1-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e44e1-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e44e1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e44e1-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e44e1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e44e1-107">DESCRIPTION</span></span>
<span data-ttu-id="e44e1-108">Das Cmdlet **enable-AzureRmOperationalInsightsIISLogCollection** startet die Sammlung von Internet Informationsdienste (IIS)-Protokollen von verbundenen Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="e44e1-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="e44e1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e44e1-109">EXAMPLES</span></span>

## <span data-ttu-id="e44e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e44e1-110">PARAMETERS</span></span>

### <span data-ttu-id="e44e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44e1-111">-DefaultProfile</span></span>
<span data-ttu-id="e44e1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e44e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e44e1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44e1-113">-ResourceGroupName</span></span>
<span data-ttu-id="e44e1-114">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="e44e1-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="e44e1-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="e44e1-115">-Workspace</span></span>
<span data-ttu-id="e44e1-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e44e1-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e44e1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e44e1-117">-WorkspaceName</span></span>
<span data-ttu-id="e44e1-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e44e1-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e44e1-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e44e1-119">-Confirm</span></span>
<span data-ttu-id="e44e1-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e44e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e44e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44e1-121">-WhatIf</span></span>
<span data-ttu-id="e44e1-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e44e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44e1-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e44e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e44e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44e1-124">CommonParameters</span></span>
<span data-ttu-id="e44e1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44e1-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44e1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44e1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e44e1-127">INPUTS</span></span>

### <span data-ttu-id="e44e1-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e44e1-128">PSWorkspace</span></span>
<span data-ttu-id="e44e1-129">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e44e1-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e44e1-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e44e1-130">OUTPUTS</span></span>

### <span data-ttu-id="e44e1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e44e1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e44e1-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e44e1-132">NOTES</span></span>

## <span data-ttu-id="e44e1-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e44e1-133">RELATED LINKS</span></span>

[<span data-ttu-id="e44e1-134">Deaktivieren-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="e44e1-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


