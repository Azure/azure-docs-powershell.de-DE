---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: bcf15e36ae428277293c174df6b7a3cd55c36252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820647"
---
# <span data-ttu-id="1c9a7-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1c9a7-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="1c9a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9a7-103">Entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="1c9a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c9a7-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c9a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c9a7-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9a7-106">Das Cmdlet **Remove-AzAvailabilitySet** entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="1c9a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c9a7-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9a7-108">Beispiel 1: Entfernen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="1c9a7-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1c9a7-109">Dieser Befehl entfernt einen Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1c9a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c9a7-110">PARAMETERS</span></span>

### <span data-ttu-id="1c9a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c9a7-111">-AsJob</span></span>
<span data-ttu-id="1c9a7-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1c9a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9a7-113">-DefaultProfile</span></span>
<span data-ttu-id="1c9a7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c9a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1c9a7-115">-Force</span></span>
<span data-ttu-id="1c9a7-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9a7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1c9a7-117">-Name</span></span>
<span data-ttu-id="1c9a7-118">Der Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c9a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="1c9a7-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c9a7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c9a7-121">-Confirm</span></span>
<span data-ttu-id="1c9a7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9a7-123">-WhatIf</span></span>
<span data-ttu-id="1c9a7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c9a7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c9a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9a7-126">CommonParameters</span></span>
<span data-ttu-id="1c9a7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9a7-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9a7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c9a7-129">INPUTS</span></span>

### <span data-ttu-id="1c9a7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1c9a7-130">System.String</span></span>

## <span data-ttu-id="1c9a7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c9a7-131">OUTPUTS</span></span>

### <span data-ttu-id="1c9a7-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1c9a7-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1c9a7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c9a7-133">NOTES</span></span>

## <span data-ttu-id="1c9a7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c9a7-134">RELATED LINKS</span></span>

[<span data-ttu-id="1c9a7-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1c9a7-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="1c9a7-136">Neu – AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1c9a7-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


