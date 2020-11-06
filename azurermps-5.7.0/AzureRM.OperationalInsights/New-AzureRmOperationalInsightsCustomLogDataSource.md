---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 510148c5d700c1378b0e468bbd5e8a9206491284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505414"
---
# <span data-ttu-id="827db-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="827db-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="827db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="827db-102">SYNOPSIS</span></span>
<span data-ttu-id="827db-103">Definiert eine benutzerdefinierte Protokoll Sammlungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="827db-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="827db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="827db-104">SYNTAX</span></span>

### <span data-ttu-id="827db-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="827db-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="827db-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="827db-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="827db-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="827db-107">DESCRIPTION</span></span>
<span data-ttu-id="827db-108">Das Cmdlet **New-AzureRmOperationalInsightsCustomLogDataSource** definiert eine benutzerdefinierte Protokoll Sammlungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="827db-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="827db-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="827db-109">EXAMPLES</span></span>

## <span data-ttu-id="827db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="827db-110">PARAMETERS</span></span>

### <span data-ttu-id="827db-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="827db-111">-CustomLogRawJson</span></span>
<span data-ttu-id="827db-112">Gibt die benutzerdefinierte Sammlungs Richtlinie als unformatierte JSON-Zeichenfolge (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="827db-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="827db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827db-113">-DefaultProfile</span></span>
<span data-ttu-id="827db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="827db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="827db-115">-Force</span><span class="sxs-lookup"><span data-stu-id="827db-115">-Force</span></span>
<span data-ttu-id="827db-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="827db-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="827db-117">-Name</span><span class="sxs-lookup"><span data-stu-id="827db-117">-Name</span></span>
<span data-ttu-id="827db-118">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="827db-118">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="827db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="827db-119">-ResourceGroupName</span></span>
<span data-ttu-id="827db-120">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="827db-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="827db-121">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="827db-121">-Workspace</span></span>
<span data-ttu-id="827db-122">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="827db-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="827db-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="827db-123">-WorkspaceName</span></span>
<span data-ttu-id="827db-124">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="827db-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="827db-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="827db-125">-Confirm</span></span>
<span data-ttu-id="827db-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="827db-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="827db-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="827db-127">-WhatIf</span></span>
<span data-ttu-id="827db-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="827db-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="827db-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="827db-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="827db-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827db-130">CommonParameters</span></span>
<span data-ttu-id="827db-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="827db-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827db-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827db-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827db-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="827db-133">INPUTS</span></span>

### <span data-ttu-id="827db-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="827db-134">PSWorkspace</span></span>
<span data-ttu-id="827db-135">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="827db-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="827db-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="827db-136">OUTPUTS</span></span>

### <span data-ttu-id="827db-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="827db-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="827db-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="827db-138">NOTES</span></span>

## <span data-ttu-id="827db-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="827db-139">RELATED LINKS</span></span>

[<span data-ttu-id="827db-140">Deaktivieren-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="827db-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="827db-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="827db-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


