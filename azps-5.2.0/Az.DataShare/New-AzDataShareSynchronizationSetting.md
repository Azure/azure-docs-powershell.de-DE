---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: df8f61b10750f50bef1b3417da7f28be4ec0d0d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290303"
---
# <span data-ttu-id="09b64-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="09b64-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="09b64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09b64-102">SYNOPSIS</span></span>
<span data-ttu-id="09b64-103">Erstellt die Synchronisierungseinstellung für eine Freigabe.</span><span class="sxs-lookup"><span data-stu-id="09b64-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="09b64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09b64-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09b64-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09b64-105">DESCRIPTION</span></span>
<span data-ttu-id="09b64-106">Das **New-AzDataShareSynchronizationSetting** erstellt eine Synchronisierungseinstellung für die Freigabe im Freigabekonto für ein wiederkehrendes Intervall von täglich oder stündlich zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="09b64-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="09b64-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09b64-107">EXAMPLES</span></span>

### <span data-ttu-id="09b64-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09b64-108">Example 1</span></span>
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

<span data-ttu-id="09b64-109">Mit diesen Befehlen wird eine Synchronisierungseinstellung für das tägliche Serienintervall um 9:00 Uhr erstellt, um AdsShare im WikiAds des Datenfreigabekontos zu teilen.</span><span class="sxs-lookup"><span data-stu-id="09b64-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="09b64-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09b64-110">PARAMETERS</span></span>

### <span data-ttu-id="09b64-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09b64-111">-AccountName</span></span>
<span data-ttu-id="09b64-112">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="09b64-112">Azure data share account name</span></span>

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

### <span data-ttu-id="09b64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b64-113">-DefaultProfile</span></span>
<span data-ttu-id="09b64-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09b64-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09b64-115">-Name</span><span class="sxs-lookup"><span data-stu-id="09b64-115">-Name</span></span>
<span data-ttu-id="09b64-116">Name der Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="09b64-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="09b64-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="09b64-117">-RecurrenceInterval</span></span>
<span data-ttu-id="09b64-118">Das Wiederholungsintervall für die Synchronisierungseinstellung (Tag oder Stunde)</span><span class="sxs-lookup"><span data-stu-id="09b64-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="09b64-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09b64-119">-ResourceGroupName</span></span>
<span data-ttu-id="09b64-120">Ressourcengruppenname des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="09b64-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="09b64-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="09b64-121">-ShareName</span></span>
<span data-ttu-id="09b64-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="09b64-122">Azure data share name</span></span>

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

### <span data-ttu-id="09b64-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="09b64-123">-SynchronizationTime</span></span>
<span data-ttu-id="09b64-124">Die Startzeit der Einstellung für die geplante Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="09b64-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="09b64-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09b64-125">-Confirm</span></span>
<span data-ttu-id="09b64-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09b64-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09b64-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="09b64-127">-WhatIf</span></span>
<span data-ttu-id="09b64-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09b64-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09b64-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09b64-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09b64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b64-130">CommonParameters</span></span>
<span data-ttu-id="09b64-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b64-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09b64-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b64-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09b64-133">INPUTS</span></span>

### <span data-ttu-id="09b64-134">Keine</span><span class="sxs-lookup"><span data-stu-id="09b64-134">None</span></span>

## <span data-ttu-id="09b64-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09b64-135">OUTPUTS</span></span>

### <span data-ttu-id="09b64-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="09b64-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="09b64-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09b64-137">NOTES</span></span>

## <span data-ttu-id="09b64-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09b64-138">RELATED LINKS</span></span>
