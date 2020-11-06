---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505133"
---
# <span data-ttu-id="8fd2c-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8fd2c-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="8fd2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd2c-103">Aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fd2c-104">SYNTAX</span></span>

### <span data-ttu-id="8fd2c-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd2c-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd2c-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="8fd2c-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd2c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fd2c-107">DESCRIPTION</span></span>
<span data-ttu-id="8fd2c-108">Das Cmdlet **Update-AzureRmAvailabilitySet** aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="8fd2c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fd2c-109">EXAMPLES</span></span>

### <span data-ttu-id="8fd2c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8fd2c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="8fd2c-111">Mit diesem Befehl wird der Verfügbarkeits Satz mit dem Namen "AvSet01" in der Ressourcengruppe "ResourceGroup01" auf einen verwalteten Verfügbarkeits Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="8fd2c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fd2c-112">PARAMETERS</span></span>

### <span data-ttu-id="8fd2c-113">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="8fd2c-113">-AvailabilitySet</span></span>
<span data-ttu-id="8fd2c-114">Gibt das Verfügbarkeits Satz Objekt an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="8fd2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd2c-115">-DefaultProfile</span></span>
<span data-ttu-id="8fd2c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fd2c-117">– Verwaltet</span><span class="sxs-lookup"><span data-stu-id="8fd2c-117">-Managed</span></span>
<span data-ttu-id="8fd2c-118">Verwalteter Verfügbarkeits Satz</span><span class="sxs-lookup"><span data-stu-id="8fd2c-118">Managed Availability Set</span></span>

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

### <span data-ttu-id="8fd2c-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="8fd2c-119">-Sku</span></span>
<span data-ttu-id="8fd2c-120">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="8fd2c-120">The Name of Sku</span></span>

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

### <span data-ttu-id="8fd2c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fd2c-121">-Confirm</span></span>
<span data-ttu-id="8fd2c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd2c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd2c-123">-WhatIf</span></span>
<span data-ttu-id="8fd2c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fd2c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd2c-126">CommonParameters</span></span>
<span data-ttu-id="8fd2c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd2c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd2c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd2c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fd2c-129">INPUTS</span></span>

### <span data-ttu-id="8fd2c-130">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8fd2c-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="8fd2c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fd2c-131">OUTPUTS</span></span>

### <span data-ttu-id="8fd2c-132">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8fd2c-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="8fd2c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fd2c-133">NOTES</span></span>

## <span data-ttu-id="8fd2c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fd2c-134">RELATED LINKS</span></span>

