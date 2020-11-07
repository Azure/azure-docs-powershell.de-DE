---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: d1a1633303e30fc10c5eee7432101fa075f4d38f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824092"
---
# <span data-ttu-id="ed5d0-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="ed5d0-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="ed5d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5d0-103">Erstellt eine Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-103">Creates a computer group.</span></span>

## <span data-ttu-id="ed5d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed5d0-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed5d0-105">DESCRIPTION</span></span>
<span data-ttu-id="ed5d0-106">Das Cmdlet **New-AzOperationalInsightsComputerGroup** erstellt eine Computergruppe in einer Ressourcengruppe und einem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="ed5d0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed5d0-107">EXAMPLES</span></span>

## <span data-ttu-id="ed5d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed5d0-108">PARAMETERS</span></span>

### <span data-ttu-id="ed5d0-109">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="ed5d0-109">-Category</span></span>
<span data-ttu-id="ed5d0-110">Gibt die Kategorie der Computergruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-110">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5d0-111">-DefaultProfile</span></span>
<span data-ttu-id="ed5d0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ed5d0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed5d0-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed5d0-113">-DisplayName</span></span>
<span data-ttu-id="ed5d0-114">Gibt den Anzeigenamen der Computergruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5d0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ed5d0-115">-Force</span></span>
<span data-ttu-id="ed5d0-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5d0-117">-Query</span><span class="sxs-lookup"><span data-stu-id="ed5d0-117">-Query</span></span>
<span data-ttu-id="ed5d0-118">Gibt die Abfrage der Computergruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5d0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5d0-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed5d0-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ed5d0-121">Das Cmdlet erstellt eine Computergruppe in dieser Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5d0-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ed5d0-122">-SavedSearchId</span></span>
<span data-ttu-id="ed5d0-123">Gibt die ID der Computergruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5d0-124">-Version</span><span class="sxs-lookup"><span data-stu-id="ed5d0-124">-Version</span></span>
<span data-ttu-id="ed5d0-125">Gibt die Version an.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5d0-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed5d0-126">-WorkspaceName</span></span>
<span data-ttu-id="ed5d0-127">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5d0-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed5d0-128">-Confirm</span></span>
<span data-ttu-id="ed5d0-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5d0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5d0-130">-WhatIf</span></span>
<span data-ttu-id="ed5d0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5d0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5d0-133">CommonParameters</span></span>
<span data-ttu-id="ed5d0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5d0-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed5d0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5d0-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed5d0-136">INPUTS</span></span>

### <span data-ttu-id="ed5d0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ed5d0-137">System.String</span></span>

### <span data-ttu-id="ed5d0-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="ed5d0-138">System.Int64</span></span>

## <span data-ttu-id="ed5d0-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed5d0-139">OUTPUTS</span></span>

### <span data-ttu-id="ed5d0-140">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="ed5d0-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="ed5d0-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed5d0-141">NOTES</span></span>

## <span data-ttu-id="ed5d0-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed5d0-142">RELATED LINKS</span></span>
