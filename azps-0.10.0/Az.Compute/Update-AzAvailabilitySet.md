---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842443"
---
# <span data-ttu-id="7054f-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7054f-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="7054f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7054f-102">SYNOPSIS</span></span>
<span data-ttu-id="7054f-103">Aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="7054f-103">Updates an availability set.</span></span>

## <span data-ttu-id="7054f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7054f-104">SYNTAX</span></span>

### <span data-ttu-id="7054f-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="7054f-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7054f-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="7054f-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7054f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7054f-107">DESCRIPTION</span></span>
<span data-ttu-id="7054f-108">Das Cmdlet **Update-AzAvailabilitySet** aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="7054f-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="7054f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7054f-109">EXAMPLES</span></span>

### <span data-ttu-id="7054f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7054f-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="7054f-111">Mit diesem Befehl wird der Verfügbarkeits Satz mit dem Namen "AvSet01" in der Ressourcengruppe "ResourceGroup01" auf einen verwalteten Verfügbarkeits Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7054f-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="7054f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7054f-112">PARAMETERS</span></span>

### <span data-ttu-id="7054f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7054f-113">-AsJob</span></span>
<span data-ttu-id="7054f-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="7054f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7054f-115">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="7054f-115">-AvailabilitySet</span></span>
<span data-ttu-id="7054f-116">Gibt das Verfügbarkeits Satz Objekt an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7054f-116">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7054f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7054f-117">-DefaultProfile</span></span>
<span data-ttu-id="7054f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7054f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7054f-119">– Verwaltet</span><span class="sxs-lookup"><span data-stu-id="7054f-119">-Managed</span></span>
<span data-ttu-id="7054f-120">Verwalteter Verfügbarkeits Satz</span><span class="sxs-lookup"><span data-stu-id="7054f-120">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7054f-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="7054f-121">-Sku</span></span>
<span data-ttu-id="7054f-122">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="7054f-122">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7054f-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7054f-123">-Confirm</span></span>
<span data-ttu-id="7054f-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7054f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7054f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7054f-125">-WhatIf</span></span>
<span data-ttu-id="7054f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7054f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7054f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7054f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7054f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7054f-128">CommonParameters</span></span>
<span data-ttu-id="7054f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7054f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7054f-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7054f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7054f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7054f-131">INPUTS</span></span>

### <span data-ttu-id="7054f-132">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7054f-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7054f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7054f-133">OUTPUTS</span></span>

### <span data-ttu-id="7054f-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7054f-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7054f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7054f-135">NOTES</span></span>

## <span data-ttu-id="7054f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7054f-136">RELATED LINKS</span></span>

