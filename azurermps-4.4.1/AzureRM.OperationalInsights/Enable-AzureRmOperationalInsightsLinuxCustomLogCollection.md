---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0b907f07280eae32ecb208fd13195767145c9541
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501702"
---
# <span data-ttu-id="5fd00-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="5fd00-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="5fd00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5fd00-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd00-103">Startet eine Sammlung von benutzerdefinierten Protokollen von Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="5fd00-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fd00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fd00-104">SYNTAX</span></span>

### <span data-ttu-id="5fd00-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5fd00-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd00-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5fd00-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd00-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fd00-107">DESCRIPTION</span></span>
<span data-ttu-id="5fd00-108">Mit dem Cmdlet **enable-AzureRmOperationalInsightsLinuxCustomLogCollection** wird eine Sammlung von benutzerdefinierten Protokollen von verbundenen Linux-Computern in einem Arbeitsbereich gestartet.</span><span class="sxs-lookup"><span data-stu-id="5fd00-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="5fd00-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5fd00-109">EXAMPLES</span></span>

## <span data-ttu-id="5fd00-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fd00-110">PARAMETERS</span></span>

### <span data-ttu-id="5fd00-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd00-111">-ResourceGroupName</span></span>
<span data-ttu-id="5fd00-112">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="5fd00-112">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="5fd00-113">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="5fd00-113">-Workspace</span></span>
<span data-ttu-id="5fd00-114">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5fd00-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5fd00-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5fd00-115">-WorkspaceName</span></span>
<span data-ttu-id="5fd00-116">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5fd00-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5fd00-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5fd00-117">-Confirm</span></span>
<span data-ttu-id="5fd00-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5fd00-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd00-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd00-119">-WhatIf</span></span>
<span data-ttu-id="5fd00-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5fd00-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd00-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fd00-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd00-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd00-122">-DefaultProfile</span></span>
<span data-ttu-id="5fd00-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fd00-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fd00-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd00-124">CommonParameters</span></span>
<span data-ttu-id="5fd00-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd00-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd00-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd00-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd00-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5fd00-127">INPUTS</span></span>

### <span data-ttu-id="5fd00-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5fd00-128">PSWorkspace</span></span>
<span data-ttu-id="5fd00-129">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5fd00-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="5fd00-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5fd00-130">OUTPUTS</span></span>

### <span data-ttu-id="5fd00-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5fd00-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5fd00-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="5fd00-132">NOTES</span></span>
* <span data-ttu-id="5fd00-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="5fd00-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5fd00-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5fd00-134">RELATED LINKS</span></span>

[<span data-ttu-id="5fd00-135">Deaktivieren-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="5fd00-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


