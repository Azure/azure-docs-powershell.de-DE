---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1e6f6957adc8a67e1d92c0aad6f2be035b4f390d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924176"
---
# <span data-ttu-id="8bd89-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8bd89-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8bd89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bd89-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd89-103">Entfernt eine angegebene Azure Data Lake Analytics-Computerichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8bd89-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="8bd89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bd89-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd89-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bd89-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd89-106">Die **Remove-AzDataLakeAnalyticsComputePolicy** entfernt eine angegebene Azure Data Lake Analytics-Computerichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8bd89-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="8bd89-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8bd89-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd89-108">Beispiel 1: Entfernen einer Datenverarbeitungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8bd89-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="8bd89-109">Mit diesem Befehl wird die angegebene Computerichtlinie mit dem Namen "myPolicy" im Konto "contosoadla" entfernt.</span><span class="sxs-lookup"><span data-stu-id="8bd89-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="8bd89-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8bd89-110">PARAMETERS</span></span>

### <span data-ttu-id="8bd89-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="8bd89-111">-Account</span></span>
<span data-ttu-id="8bd89-112">Name des Kontos, aus dem die Datenverarbeitungsrichtlinie entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bd89-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="8bd89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd89-113">-DefaultProfile</span></span>
<span data-ttu-id="8bd89-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8bd89-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bd89-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8bd89-115">-Name</span></span>
<span data-ttu-id="8bd89-116">Name der zu entfernende Datenverarbeitungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8bd89-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="8bd89-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bd89-117">-PassThru</span></span>
<span data-ttu-id="8bd89-118">Geben Sie "True" nach dem erfolgreichen Löschen zurück.</span><span class="sxs-lookup"><span data-stu-id="8bd89-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="8bd89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd89-119">-ResourceGroupName</span></span>
<span data-ttu-id="8bd89-120">Name der Ressourcengruppe, unter der Sie das Konto haben.</span><span class="sxs-lookup"><span data-stu-id="8bd89-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="8bd89-121">Optional und versucht zu ermitteln, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="8bd89-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="8bd89-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8bd89-122">-Confirm</span></span>
<span data-ttu-id="8bd89-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bd89-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd89-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd89-124">-WhatIf</span></span>
<span data-ttu-id="8bd89-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bd89-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bd89-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bd89-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd89-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd89-127">CommonParameters</span></span>
<span data-ttu-id="8bd89-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd89-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd89-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bd89-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd89-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8bd89-130">INPUTS</span></span>

### <span data-ttu-id="8bd89-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8bd89-131">System.String</span></span>

## <span data-ttu-id="8bd89-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8bd89-132">OUTPUTS</span></span>

### <span data-ttu-id="8bd89-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8bd89-133">System.Boolean</span></span>

## <span data-ttu-id="8bd89-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8bd89-134">NOTES</span></span>

## <span data-ttu-id="8bd89-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8bd89-135">RELATED LINKS</span></span>
