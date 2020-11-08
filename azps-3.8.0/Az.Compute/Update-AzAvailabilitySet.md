---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004798"
---
# <span data-ttu-id="946b7-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="946b7-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="946b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="946b7-102">SYNOPSIS</span></span>
<span data-ttu-id="946b7-103">Aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="946b7-103">Updates an availability set.</span></span>

## <span data-ttu-id="946b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="946b7-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="946b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="946b7-105">DESCRIPTION</span></span>
<span data-ttu-id="946b7-106">Das Cmdlet **Update-AzAvailabilitySet** aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="946b7-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="946b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="946b7-107">EXAMPLES</span></span>

### <span data-ttu-id="946b7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="946b7-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="946b7-109">Mit diesem Befehl wird der Verfügbarkeits Satz mit dem Namen "AvSet01" in der Ressourcengruppe "ResourceGroup01" auf einen verwalteten Verfügbarkeits Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="946b7-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="946b7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="946b7-110">PARAMETERS</span></span>

### <span data-ttu-id="946b7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="946b7-111">-AsJob</span></span>
<span data-ttu-id="946b7-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="946b7-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="946b7-113">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="946b7-113">-AvailabilitySet</span></span>
<span data-ttu-id="946b7-114">Gibt das Verfügbarkeits Satz Objekt an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="946b7-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="946b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946b7-115">-DefaultProfile</span></span>
<span data-ttu-id="946b7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="946b7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="946b7-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="946b7-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="946b7-118">Die Ressourcen-ID der für diesen Verfügbarkeits Satz zu verwendenden Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="946b7-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946b7-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="946b7-119">-Sku</span></span>
<span data-ttu-id="946b7-120">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="946b7-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946b7-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="946b7-121">-Tag</span></span>
<span data-ttu-id="946b7-122">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="946b7-122">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946b7-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="946b7-123">-Confirm</span></span>
<span data-ttu-id="946b7-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="946b7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946b7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="946b7-125">-WhatIf</span></span>
<span data-ttu-id="946b7-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="946b7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="946b7-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="946b7-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946b7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946b7-128">CommonParameters</span></span>
<span data-ttu-id="946b7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="946b7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946b7-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="946b7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946b7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="946b7-131">INPUTS</span></span>

### <span data-ttu-id="946b7-132">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="946b7-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="946b7-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="946b7-133">OUTPUTS</span></span>

### <span data-ttu-id="946b7-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="946b7-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="946b7-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="946b7-135">NOTES</span></span>

## <span data-ttu-id="946b7-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="946b7-136">RELATED LINKS</span></span>
