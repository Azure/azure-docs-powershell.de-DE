---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 8a54a735b41ef537a31f5e3e1ce2789d10e60af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496997"
---
# <span data-ttu-id="4d07c-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="4d07c-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="4d07c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d07c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d07c-103">Erstellt eine Computergruppe.</span><span class="sxs-lookup"><span data-stu-id="4d07c-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d07c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d07c-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d07c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d07c-105">DESCRIPTION</span></span>
<span data-ttu-id="4d07c-106">Das Cmdlet **New-AzureRmOperationalInsightsComputerGroup** erstellt eine Computergruppe in einer Ressourcengruppe und einem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="4d07c-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="4d07c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d07c-107">EXAMPLES</span></span>

## <span data-ttu-id="4d07c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d07c-108">PARAMETERS</span></span>

### <span data-ttu-id="4d07c-109">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="4d07c-109">-Category</span></span>
<span data-ttu-id="4d07c-110">Gibt die Kategorie der Computergruppe an.</span><span class="sxs-lookup"><span data-stu-id="4d07c-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="4d07c-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4d07c-111">-DisplayName</span></span>
<span data-ttu-id="4d07c-112">Gibt den Anzeigenamen der Computergruppe an.</span><span class="sxs-lookup"><span data-stu-id="4d07c-112">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="4d07c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4d07c-113">-Force</span></span>
<span data-ttu-id="4d07c-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4d07c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d07c-115">-Query</span><span class="sxs-lookup"><span data-stu-id="4d07c-115">-Query</span></span>
<span data-ttu-id="4d07c-116">Gibt die Abfrage der Computergruppe an.</span><span class="sxs-lookup"><span data-stu-id="4d07c-116">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="4d07c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d07c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d07c-118">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4d07c-118">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4d07c-119">Das Cmdlet erstellt eine Computergruppe in dieser Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d07c-119">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="4d07c-120">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="4d07c-120">-SavedSearchId</span></span>
<span data-ttu-id="4d07c-121">Gibt die ID der Computergruppe an.</span><span class="sxs-lookup"><span data-stu-id="4d07c-121">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="4d07c-122">-Version</span><span class="sxs-lookup"><span data-stu-id="4d07c-122">-Version</span></span>
<span data-ttu-id="4d07c-123">Gibt die Version an.</span><span class="sxs-lookup"><span data-stu-id="4d07c-123">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d07c-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d07c-124">-WorkspaceName</span></span>
<span data-ttu-id="4d07c-125">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="4d07c-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="4d07c-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d07c-126">-Confirm</span></span>
<span data-ttu-id="4d07c-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d07c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d07c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d07c-128">-WhatIf</span></span>
<span data-ttu-id="4d07c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d07c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d07c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d07c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d07c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d07c-131">-DefaultProfile</span></span>
<span data-ttu-id="4d07c-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d07c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d07c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d07c-133">CommonParameters</span></span>
<span data-ttu-id="4d07c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d07c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d07c-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d07c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d07c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d07c-136">INPUTS</span></span>

## <span data-ttu-id="4d07c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d07c-137">OUTPUTS</span></span>

## <span data-ttu-id="4d07c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d07c-138">NOTES</span></span>

## <span data-ttu-id="4d07c-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d07c-139">RELATED LINKS</span></span>

