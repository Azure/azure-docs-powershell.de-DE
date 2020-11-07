---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: deafb0cb68ab58997df83bc0280b50a4cc4a0de0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661293"
---
# <span data-ttu-id="25562-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="25562-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="25562-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25562-102">SYNOPSIS</span></span>
<span data-ttu-id="25562-103">Entfernt eine angegebene Azure Data Lake-Analyse Compute-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="25562-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="25562-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25562-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25562-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25562-105">DESCRIPTION</span></span>
<span data-ttu-id="25562-106">Die **Remove-AzDataLakeAnalyticsComputePolicy-** Funktion entfernt eine angegebene Azure Data Lake Analytics-Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="25562-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="25562-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25562-107">EXAMPLES</span></span>

### <span data-ttu-id="25562-108">Beispiel 1: Entfernen einer COMPUTE-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="25562-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="25562-109">Mit diesem Befehl wird die angegebene Compute-Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" entfernt.</span><span class="sxs-lookup"><span data-stu-id="25562-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="25562-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25562-110">PARAMETERS</span></span>

### <span data-ttu-id="25562-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="25562-111">-Account</span></span>
<span data-ttu-id="25562-112">Der Name des Kontos, aus dem die Compute-Richtlinie entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25562-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="25562-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25562-113">-DefaultProfile</span></span>
<span data-ttu-id="25562-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="25562-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25562-115">-Name</span><span class="sxs-lookup"><span data-stu-id="25562-115">-Name</span></span>
<span data-ttu-id="25562-116">Der Name der zu entfernenden Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="25562-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="25562-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25562-117">-PassThru</span></span>
<span data-ttu-id="25562-118">Beim erfolgreichen löschen wird true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25562-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="25562-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25562-119">-ResourceGroupName</span></span>
<span data-ttu-id="25562-120">Name der Ressourcengruppe, unter der Sie das Konto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="25562-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="25562-121">Optional und versucht, festzustellen, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="25562-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="25562-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25562-122">-Confirm</span></span>
<span data-ttu-id="25562-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25562-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25562-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25562-124">-WhatIf</span></span>
<span data-ttu-id="25562-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25562-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25562-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25562-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25562-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25562-127">CommonParameters</span></span>
<span data-ttu-id="25562-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25562-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25562-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25562-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25562-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25562-130">INPUTS</span></span>

### <span data-ttu-id="25562-131">System. String</span><span class="sxs-lookup"><span data-stu-id="25562-131">System.String</span></span>

## <span data-ttu-id="25562-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25562-132">OUTPUTS</span></span>

### <span data-ttu-id="25562-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25562-133">System.Boolean</span></span>

## <span data-ttu-id="25562-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="25562-134">NOTES</span></span>

## <span data-ttu-id="25562-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25562-135">RELATED LINKS</span></span>
