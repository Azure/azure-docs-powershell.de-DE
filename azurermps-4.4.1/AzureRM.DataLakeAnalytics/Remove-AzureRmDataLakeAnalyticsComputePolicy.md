---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8be60712f0687edcbd036c48a079e3ecb90ec6c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501913"
---
# <span data-ttu-id="fa9c1-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fa9c1-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fa9c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa9c1-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9c1-103">Entfernt eine angegebene Azure Data Lake-Analyse Compute-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="fa9c1-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa9c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa9c1-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9c1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa9c1-105">DESCRIPTION</span></span>
<span data-ttu-id="fa9c1-106">Die **Remove-AzureRmDataLakeAnalyticsComputePolicy-** Funktion entfernt eine angegebene Azure Data Lake Analytics-Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="fa9c1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa9c1-107">EXAMPLES</span></span>

### <span data-ttu-id="fa9c1-108">Beispiel 1: Entfernen einer COMPUTE-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="fa9c1-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="fa9c1-109">Mit diesem Befehl wird die angegebene Compute-Richtlinie mit dem Namen "meine Richtlinie" im Konto "contosoadla" entfernt.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="fa9c1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa9c1-110">PARAMETERS</span></span>

### <span data-ttu-id="fa9c1-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="fa9c1-111">-Account</span></span>
<span data-ttu-id="fa9c1-112">Der Name des Kontos, aus dem die Compute-Richtlinie entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="fa9c1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fa9c1-113">-Name</span></span>
<span data-ttu-id="fa9c1-114">Der Name der zu entfernenden Compute-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-114">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="fa9c1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa9c1-115">-PassThru</span></span>
<span data-ttu-id="fa9c1-116">Beim erfolgreichen löschen wird true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-116">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="fa9c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa9c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa9c1-118">Name der Ressourcengruppe, unter der Sie das Konto vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="fa9c1-119">Optional und versucht, festzustellen, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="fa9c1-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa9c1-120">-Confirm</span></span>
<span data-ttu-id="fa9c1-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9c1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9c1-122">-WhatIf</span></span>
<span data-ttu-id="fa9c1-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9c1-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9c1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9c1-125">-DefaultProfile</span></span>
<span data-ttu-id="fa9c1-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa9c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9c1-127">CommonParameters</span></span>
<span data-ttu-id="fa9c1-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa9c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9c1-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa9c1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9c1-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa9c1-130">INPUTS</span></span>

### <span data-ttu-id="fa9c1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fa9c1-131">System.String</span></span>

## <span data-ttu-id="fa9c1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa9c1-132">OUTPUTS</span></span>

### <span data-ttu-id="fa9c1-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa9c1-133">System.Boolean</span></span>

## <span data-ttu-id="fa9c1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa9c1-134">NOTES</span></span>

## <span data-ttu-id="fa9c1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa9c1-135">RELATED LINKS</span></span>

