---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 5632aed8c1b3dde653be65fd587be5f1adf9cbbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941843"
---
# <span data-ttu-id="7e87f-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="7e87f-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="7e87f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e87f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e87f-103">Erstellt die Synchronisierungseinstellung für eine Freigabe.</span><span class="sxs-lookup"><span data-stu-id="7e87f-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="7e87f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e87f-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e87f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e87f-105">DESCRIPTION</span></span>
<span data-ttu-id="7e87f-106">Das **New-AzDataShareSynchronizationSetting** erstellt eine Synchronisierungseinstellung für die Freigabe im Freigabekonto für ein Serienintervall von entweder täglich oder stündlich zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="7e87f-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="7e87f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e87f-107">EXAMPLES</span></span>

### <span data-ttu-id="7e87f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7e87f-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="7e87f-109">Mit diesen Befehlen wird eine Synchronisierungseinstellung für das tägliche Serienintervall um 9:00 Uhr für die Freigabe von AdsShare im WikiAds des Datenfreigabekontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e87f-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="7e87f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7e87f-110">PARAMETERS</span></span>

### <span data-ttu-id="7e87f-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e87f-111">-AccountName</span></span>
<span data-ttu-id="7e87f-112">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="7e87f-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e87f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e87f-113">-DefaultProfile</span></span>
<span data-ttu-id="7e87f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e87f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e87f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7e87f-115">-Name</span></span>
<span data-ttu-id="7e87f-116">Name der Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="7e87f-116">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e87f-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="7e87f-117">-RecurrenceInterval</span></span>
<span data-ttu-id="7e87f-118">Das Serienintervall für die Synchronisierungseinstellung (Tag oder Stunde)</span><span class="sxs-lookup"><span data-stu-id="7e87f-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e87f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e87f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e87f-120">Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="7e87f-120">Resource group name of azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e87f-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7e87f-121">-ShareName</span></span>
<span data-ttu-id="7e87f-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="7e87f-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e87f-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="7e87f-123">-SynchronizationTime</span></span>
<span data-ttu-id="7e87f-124">Die Startzeit der geplanten Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="7e87f-124">The start time of the scheduled synchronization setting</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e87f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e87f-125">-Confirm</span></span>
<span data-ttu-id="7e87f-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e87f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e87f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e87f-127">-WhatIf</span></span>
<span data-ttu-id="7e87f-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e87f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e87f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e87f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e87f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e87f-130">CommonParameters</span></span>
<span data-ttu-id="7e87f-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e87f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e87f-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e87f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e87f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e87f-133">INPUTS</span></span>

### <span data-ttu-id="7e87f-134">Keine</span><span class="sxs-lookup"><span data-stu-id="7e87f-134">None</span></span>

## <span data-ttu-id="7e87f-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e87f-135">OUTPUTS</span></span>

### <span data-ttu-id="7e87f-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="7e87f-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="7e87f-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7e87f-137">NOTES</span></span>

## <span data-ttu-id="7e87f-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7e87f-138">RELATED LINKS</span></span>
