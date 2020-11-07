---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: ebb6635cd593e37eedf4a8e70230cbf0f42e0d92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651871"
---
# <span data-ttu-id="453a7-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="453a7-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="453a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="453a7-102">SYNOPSIS</span></span>
<span data-ttu-id="453a7-103">Aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="453a7-103">Updates an availability set.</span></span>

## <span data-ttu-id="453a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="453a7-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="453a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="453a7-105">DESCRIPTION</span></span>
<span data-ttu-id="453a7-106">Das Cmdlet **Update-AzAvailabilitySet** aktualisiert einen Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="453a7-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="453a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="453a7-107">EXAMPLES</span></span>

### <span data-ttu-id="453a7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="453a7-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="453a7-109">Mit diesem Befehl wird der Verfügbarkeits Satz mit dem Namen "AvSet01" in der Ressourcengruppe "ResourceGroup01" auf einen verwalteten Verfügbarkeits Satz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="453a7-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="453a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="453a7-110">PARAMETERS</span></span>

### <span data-ttu-id="453a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="453a7-111">-AsJob</span></span>
<span data-ttu-id="453a7-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="453a7-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="453a7-113">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="453a7-113">-AvailabilitySet</span></span>
<span data-ttu-id="453a7-114">Gibt das Verfügbarkeits Satz Objekt an, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="453a7-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="453a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453a7-115">-DefaultProfile</span></span>
<span data-ttu-id="453a7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="453a7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="453a7-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="453a7-117">-Sku</span></span>
<span data-ttu-id="453a7-118">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="453a7-118">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453a7-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="453a7-119">-Tag</span></span>
<span data-ttu-id="453a7-120">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="453a7-120">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="453a7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="453a7-121">-Confirm</span></span>
<span data-ttu-id="453a7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="453a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="453a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="453a7-123">-WhatIf</span></span>
<span data-ttu-id="453a7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="453a7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="453a7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="453a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="453a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453a7-126">CommonParameters</span></span>
<span data-ttu-id="453a7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="453a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453a7-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="453a7-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453a7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="453a7-129">INPUTS</span></span>

### <span data-ttu-id="453a7-130">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="453a7-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="453a7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="453a7-131">OUTPUTS</span></span>

### <span data-ttu-id="453a7-132">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="453a7-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="453a7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="453a7-133">NOTES</span></span>

## <span data-ttu-id="453a7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="453a7-134">RELATED LINKS</span></span>
