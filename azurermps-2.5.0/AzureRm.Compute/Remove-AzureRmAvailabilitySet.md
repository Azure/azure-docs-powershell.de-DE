---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: cc8292940a252844c0aeabe820eec2e62055c954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850092"
---
# <span data-ttu-id="85fdb-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85fdb-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="85fdb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="85fdb-103">Entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="85fdb-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85fdb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85fdb-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85fdb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85fdb-105">DESCRIPTION</span></span>
<span data-ttu-id="85fdb-106">Das Cmdlet **Remove-AzureRmAvailabilitySet** entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="85fdb-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="85fdb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85fdb-107">EXAMPLES</span></span>

### <span data-ttu-id="85fdb-108">Beispiel 1: Entfernen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="85fdb-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="85fdb-109">Dieser Befehl entfernt einen Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="85fdb-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="85fdb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="85fdb-110">PARAMETERS</span></span>

### <span data-ttu-id="85fdb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85fdb-111">-AsJob</span></span>
<span data-ttu-id="85fdb-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="85fdb-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="85fdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85fdb-113">-DefaultProfile</span></span>
<span data-ttu-id="85fdb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85fdb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85fdb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="85fdb-115">-Force</span></span>
<span data-ttu-id="85fdb-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="85fdb-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85fdb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="85fdb-117">-Name</span></span>
<span data-ttu-id="85fdb-118">Der Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="85fdb-118">The availability set name.</span></span>

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

### <span data-ttu-id="85fdb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85fdb-119">-ResourceGroupName</span></span>
<span data-ttu-id="85fdb-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="85fdb-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85fdb-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85fdb-121">-Confirm</span></span>
<span data-ttu-id="85fdb-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85fdb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85fdb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85fdb-123">-WhatIf</span></span>
<span data-ttu-id="85fdb-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85fdb-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="85fdb-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85fdb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85fdb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85fdb-126">CommonParameters</span></span>
<span data-ttu-id="85fdb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85fdb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85fdb-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85fdb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85fdb-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85fdb-129">INPUTS</span></span>

### <span data-ttu-id="85fdb-130">Keine</span><span class="sxs-lookup"><span data-stu-id="85fdb-130">None</span></span>
<span data-ttu-id="85fdb-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="85fdb-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85fdb-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85fdb-132">OUTPUTS</span></span>

### <span data-ttu-id="85fdb-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="85fdb-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="85fdb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="85fdb-134">NOTES</span></span>

## <span data-ttu-id="85fdb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85fdb-135">RELATED LINKS</span></span>

[<span data-ttu-id="85fdb-136">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85fdb-136">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="85fdb-137">Neu – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85fdb-137">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


