---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7efbfd633b87603d22b5009be71e07895442d893
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480453"
---
# <span data-ttu-id="47920-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47920-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="47920-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47920-102">SYNOPSIS</span></span>
<span data-ttu-id="47920-103">Entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="47920-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47920-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47920-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47920-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47920-105">DESCRIPTION</span></span>
<span data-ttu-id="47920-106">Das Cmdlet **Remove-AzureRmAvailabilitySet** entfernt einen Verfügbarkeits Satz aus Azure.</span><span class="sxs-lookup"><span data-stu-id="47920-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="47920-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47920-107">EXAMPLES</span></span>

### <span data-ttu-id="47920-108">Beispiel 1: Entfernen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="47920-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="47920-109">Dieser Befehl entfernt einen Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="47920-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="47920-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="47920-110">PARAMETERS</span></span>

### <span data-ttu-id="47920-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47920-111">-AsJob</span></span>
<span data-ttu-id="47920-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="47920-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="47920-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47920-113">-DefaultProfile</span></span>
<span data-ttu-id="47920-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47920-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47920-115">-Force</span><span class="sxs-lookup"><span data-stu-id="47920-115">-Force</span></span>
<span data-ttu-id="47920-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="47920-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="47920-117">-Name</span><span class="sxs-lookup"><span data-stu-id="47920-117">-Name</span></span>
<span data-ttu-id="47920-118">Der Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="47920-118">The availability set name.</span></span>

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

### <span data-ttu-id="47920-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47920-119">-ResourceGroupName</span></span>
<span data-ttu-id="47920-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="47920-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="47920-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47920-121">-Confirm</span></span>
<span data-ttu-id="47920-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47920-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47920-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47920-123">-WhatIf</span></span>
<span data-ttu-id="47920-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47920-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47920-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47920-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47920-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47920-126">CommonParameters</span></span>
<span data-ttu-id="47920-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47920-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47920-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47920-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47920-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47920-129">INPUTS</span></span>

### <span data-ttu-id="47920-130">System. String</span><span class="sxs-lookup"><span data-stu-id="47920-130">System.String</span></span>

## <span data-ttu-id="47920-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47920-131">OUTPUTS</span></span>

### <span data-ttu-id="47920-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="47920-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="47920-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="47920-133">NOTES</span></span>

## <span data-ttu-id="47920-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47920-134">RELATED LINKS</span></span>

[<span data-ttu-id="47920-135">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47920-135">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="47920-136">Neu – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47920-136">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


