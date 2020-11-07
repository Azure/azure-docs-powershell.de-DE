---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 5a2a8157e69c1b50cc066bb24e8261c1748a6323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844435"
---
# <span data-ttu-id="0c50a-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0c50a-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="0c50a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c50a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c50a-103">Entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="0c50a-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="0c50a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c50a-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c50a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c50a-105">DESCRIPTION</span></span>
<span data-ttu-id="0c50a-106">Das Cmdlet **Remove-AzAvailabilitySet** entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="0c50a-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="0c50a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c50a-107">EXAMPLES</span></span>

### <span data-ttu-id="0c50a-108">Beispiel 1: Entfernen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="0c50a-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0c50a-109">Dieser Befehl entfernt einen Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0c50a-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="0c50a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c50a-110">PARAMETERS</span></span>

### <span data-ttu-id="0c50a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c50a-111">-AsJob</span></span>
<span data-ttu-id="0c50a-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="0c50a-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0c50a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c50a-113">-DefaultProfile</span></span>
<span data-ttu-id="0c50a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c50a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c50a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0c50a-115">-Force</span></span>
<span data-ttu-id="0c50a-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0c50a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c50a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0c50a-117">-Name</span></span>
<span data-ttu-id="0c50a-118">Der Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0c50a-118">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c50a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c50a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c50a-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0c50a-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c50a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c50a-121">-Confirm</span></span>
<span data-ttu-id="0c50a-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c50a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c50a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c50a-123">-WhatIf</span></span>
<span data-ttu-id="0c50a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c50a-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0c50a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c50a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c50a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c50a-126">CommonParameters</span></span>
<span data-ttu-id="0c50a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c50a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c50a-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c50a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c50a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c50a-129">INPUTS</span></span>

### <span data-ttu-id="0c50a-130">Keine</span><span class="sxs-lookup"><span data-stu-id="0c50a-130">None</span></span>
<span data-ttu-id="0c50a-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0c50a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c50a-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c50a-132">OUTPUTS</span></span>

### <span data-ttu-id="0c50a-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0c50a-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0c50a-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c50a-134">NOTES</span></span>

## <span data-ttu-id="0c50a-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c50a-135">RELATED LINKS</span></span>

[<span data-ttu-id="0c50a-136">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0c50a-136">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="0c50a-137">Neu – AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0c50a-137">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


