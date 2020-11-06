---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 5ae46e232cbc370947b4bc83a1148cb62a0a820d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505421"
---
# <span data-ttu-id="bac03-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bac03-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="bac03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bac03-102">SYNOPSIS</span></span>
<span data-ttu-id="bac03-103">Beendet die Sammlung benutzerdefinierter Protokolle von Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="bac03-103">Stops collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bac03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bac03-104">SYNTAX</span></span>

### <span data-ttu-id="bac03-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bac03-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bac03-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bac03-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac03-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bac03-107">DESCRIPTION</span></span>
<span data-ttu-id="bac03-108">Das Cmdlet **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** beendet die Sammlung benutzerdefinierter Protokolle von verbundenen Linux-Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="bac03-108">The **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="bac03-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bac03-109">EXAMPLES</span></span>

## <span data-ttu-id="bac03-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bac03-110">PARAMETERS</span></span>

### <span data-ttu-id="bac03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac03-111">-DefaultProfile</span></span>
<span data-ttu-id="bac03-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bac03-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bac03-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac03-113">-ResourceGroupName</span></span>
<span data-ttu-id="bac03-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="bac03-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="bac03-115">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="bac03-115">-Workspace</span></span>
<span data-ttu-id="bac03-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bac03-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bac03-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bac03-117">-WorkspaceName</span></span>
<span data-ttu-id="bac03-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bac03-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bac03-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bac03-119">-Confirm</span></span>
<span data-ttu-id="bac03-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bac03-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac03-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac03-121">-WhatIf</span></span>
<span data-ttu-id="bac03-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bac03-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bac03-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bac03-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac03-124">CommonParameters</span></span>
<span data-ttu-id="bac03-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac03-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac03-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac03-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bac03-127">INPUTS</span></span>

### <span data-ttu-id="bac03-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bac03-128">PSWorkspace</span></span>
<span data-ttu-id="bac03-129">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bac03-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bac03-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bac03-130">OUTPUTS</span></span>

### <span data-ttu-id="bac03-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bac03-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bac03-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="bac03-132">NOTES</span></span>
* <span data-ttu-id="bac03-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="bac03-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bac03-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bac03-134">RELATED LINKS</span></span>

[<span data-ttu-id="bac03-135">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bac03-135">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


