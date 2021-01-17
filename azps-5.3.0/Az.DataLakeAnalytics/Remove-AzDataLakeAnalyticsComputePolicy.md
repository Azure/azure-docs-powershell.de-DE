---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458127"
---
# <span data-ttu-id="b8b3d-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b8b3d-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="b8b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b3d-103">Entfernt eine angegebene Azure Data Lake Analytics-Rechenrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="b8b3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8b3d-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8b3d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b3d-106">Die **Remove-AzDataLakeAnalyticsComputePolicy entfernt** eine angegebene Azure Data Lake Analytics-Rechenrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="b8b3d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8b3d-107">EXAMPLES</span></span>

### <span data-ttu-id="b8b3d-108">Beispiel 1: Entfernen einer Berechnungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b8b3d-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="b8b3d-109">Mit diesem Befehl wird die angegebene Berechnungsrichtlinie mit dem Namen "myPolicy" im Konto "contosoadla" entfernt.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="b8b3d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8b3d-110">PARAMETERS</span></span>

### <span data-ttu-id="b8b3d-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b8b3d-111">-Account</span></span>
<span data-ttu-id="b8b3d-112">Name des Kontos, von dem die Berechnungsrichtlinie entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b3d-113">-DefaultProfile</span></span>
<span data-ttu-id="b8b3d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b8b3d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8b3d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b8b3d-115">-Name</span></span>
<span data-ttu-id="b8b3d-116">Name der zu entfernende Berechnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b3d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8b3d-117">-PassThru</span></span>
<span data-ttu-id="b8b3d-118">Geben Sie "true" nach erfolgreicher Löschung zurück.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="b8b3d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8b3d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b8b3d-120">Name der Ressourcengruppe, unter der Sie das Konto haben.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="b8b3d-121">Optional und wird versucht zu ermitteln, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b3d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8b3d-122">-Confirm</span></span>
<span data-ttu-id="b8b3d-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8b3d-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b8b3d-124">-WhatIf</span></span>
<span data-ttu-id="b8b3d-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8b3d-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8b3d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b3d-127">CommonParameters</span></span>
<span data-ttu-id="b8b3d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b3d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b3d-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8b3d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b3d-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8b3d-130">INPUTS</span></span>

### <span data-ttu-id="b8b3d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b8b3d-131">System.String</span></span>

## <span data-ttu-id="b8b3d-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8b3d-132">OUTPUTS</span></span>

### <span data-ttu-id="b8b3d-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8b3d-133">System.Boolean</span></span>

## <span data-ttu-id="b8b3d-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8b3d-134">NOTES</span></span>

## <span data-ttu-id="b8b3d-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8b3d-135">RELATED LINKS</span></span>
