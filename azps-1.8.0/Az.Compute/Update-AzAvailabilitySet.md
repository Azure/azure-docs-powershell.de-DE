---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4051cbb697625f527afdf2e189953c4d6e776214
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820495"
---
# <span data-ttu-id="f4e3a-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f4e3a-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="f4e3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e3a-103">Aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-103">Updates an availability set.</span></span>

## <span data-ttu-id="f4e3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4e3a-104">SYNTAX</span></span>

### <span data-ttu-id="f4e3a-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4e3a-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e3a-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="f4e3a-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e3a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="f4e3a-108">Das Cmdlet **Update-AzAvailabilitySet** aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="f4e3a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="f4e3a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4e3a-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="f4e3a-111">Mit diesem Befehl wird der Verfügbarkeits Satz mit dem Namen "AvSet01" in der Ressourcengruppe "ResourceGroup01" auf einen verwalteten Verfügbarkeits Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="f4e3a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="f4e3a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4e3a-113">-AsJob</span></span>
<span data-ttu-id="f4e3a-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f4e3a-115">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="f4e3a-115">-AvailabilitySet</span></span>
<span data-ttu-id="f4e3a-116">Gibt das Verfügbarkeits Satz Objekt an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="f4e3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e3a-117">-DefaultProfile</span></span>
<span data-ttu-id="f4e3a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e3a-119">– Verwaltet</span><span class="sxs-lookup"><span data-stu-id="f4e3a-119">-Managed</span></span>
<span data-ttu-id="f4e3a-120">Verwalteter Verfügbarkeits Satz</span><span class="sxs-lookup"><span data-stu-id="f4e3a-120">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3a-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="f4e3a-121">-Sku</span></span>
<span data-ttu-id="f4e3a-122">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="f4e3a-122">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3a-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4e3a-123">-Tag</span></span>
<span data-ttu-id="f4e3a-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="f4e3a-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="f4e3a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4e3a-125">-Confirm</span></span>
<span data-ttu-id="f4e3a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e3a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e3a-127">-WhatIf</span></span>
<span data-ttu-id="f4e3a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4e3a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e3a-130">CommonParameters</span></span>
<span data-ttu-id="f4e3a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e3a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e3a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e3a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4e3a-133">INPUTS</span></span>

### <span data-ttu-id="f4e3a-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f4e3a-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f4e3a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4e3a-135">OUTPUTS</span></span>

### <span data-ttu-id="f4e3a-136">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f4e3a-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f4e3a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4e3a-137">NOTES</span></span>

## <span data-ttu-id="f4e3a-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4e3a-138">RELATED LINKS</span></span>
