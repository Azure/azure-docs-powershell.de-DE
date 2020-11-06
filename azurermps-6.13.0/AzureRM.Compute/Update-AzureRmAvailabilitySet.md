---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499662"
---
# <span data-ttu-id="b8aeb-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b8aeb-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="b8aeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8aeb-103">Aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8aeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8aeb-104">SYNTAX</span></span>

### <span data-ttu-id="b8aeb-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8aeb-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8aeb-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="b8aeb-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8aeb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8aeb-107">DESCRIPTION</span></span>
<span data-ttu-id="b8aeb-108">Das Cmdlet **Update-AzureRmAvailabilitySet** aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="b8aeb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8aeb-109">EXAMPLES</span></span>

### <span data-ttu-id="b8aeb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8aeb-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="b8aeb-111">Mit diesem Befehl wird der Verfügbarkeits Satz mit dem Namen "AvSet01" in der Ressourcengruppe "ResourceGroup01" auf einen verwalteten Verfügbarkeits Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="b8aeb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8aeb-112">PARAMETERS</span></span>

### <span data-ttu-id="b8aeb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8aeb-113">-AsJob</span></span>
<span data-ttu-id="b8aeb-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b8aeb-115">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="b8aeb-115">-AvailabilitySet</span></span>
<span data-ttu-id="b8aeb-116">Gibt das Verfügbarkeits Satz Objekt an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="b8aeb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8aeb-117">-DefaultProfile</span></span>
<span data-ttu-id="b8aeb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8aeb-119">– Verwaltet</span><span class="sxs-lookup"><span data-stu-id="b8aeb-119">-Managed</span></span>
<span data-ttu-id="b8aeb-120">Verwalteter Verfügbarkeits Satz</span><span class="sxs-lookup"><span data-stu-id="b8aeb-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="b8aeb-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="b8aeb-121">-Sku</span></span>
<span data-ttu-id="b8aeb-122">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="b8aeb-122">The Name of Sku</span></span>

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

### <span data-ttu-id="b8aeb-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8aeb-123">-Tag</span></span>
<span data-ttu-id="b8aeb-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="b8aeb-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="b8aeb-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8aeb-125">-Confirm</span></span>
<span data-ttu-id="b8aeb-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8aeb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8aeb-127">-WhatIf</span></span>
<span data-ttu-id="b8aeb-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8aeb-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8aeb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8aeb-130">CommonParameters</span></span>
<span data-ttu-id="b8aeb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8aeb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8aeb-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8aeb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8aeb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8aeb-133">INPUTS</span></span>

### <span data-ttu-id="b8aeb-134">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b8aeb-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="b8aeb-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8aeb-135">OUTPUTS</span></span>

### <span data-ttu-id="b8aeb-136">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b8aeb-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="b8aeb-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8aeb-137">NOTES</span></span>

## <span data-ttu-id="b8aeb-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8aeb-138">RELATED LINKS</span></span>
