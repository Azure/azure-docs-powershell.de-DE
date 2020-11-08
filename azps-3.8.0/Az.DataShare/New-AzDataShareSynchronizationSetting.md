---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: d7f6429ebc3e8a3ebf1f8dd2749e6b7f66005ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996532"
---
# <span data-ttu-id="addb7-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="addb7-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="addb7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="addb7-102">SYNOPSIS</span></span>
<span data-ttu-id="addb7-103">Erstellt eine Synchronisierungseinstellung für eine Freigabe.</span><span class="sxs-lookup"><span data-stu-id="addb7-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="addb7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="addb7-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="addb7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="addb7-105">DESCRIPTION</span></span>
<span data-ttu-id="addb7-106">Das **New-AzDataShareSynchronizationSetting** erstellt eine Synchronisierungseinstellung für die Freigabe in einem Freigabe Konto für ein Serienintervall von täglich oder stündlich zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="addb7-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="addb7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="addb7-107">EXAMPLES</span></span>

### <span data-ttu-id="addb7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="addb7-108">Example 1</span></span>
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

<span data-ttu-id="addb7-109">Mit diesen Befehlen wird eine Synchronisierungseinstellung für das tägliche Serienintervall von 9:00 am für Freigabe AdsShare in Datenfreigabe Konto WikiAds erstellt.</span><span class="sxs-lookup"><span data-stu-id="addb7-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="addb7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="addb7-110">PARAMETERS</span></span>

### <span data-ttu-id="addb7-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="addb7-111">-AccountName</span></span>
<span data-ttu-id="addb7-112">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="addb7-112">Azure data share account name</span></span>

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

### <span data-ttu-id="addb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addb7-113">-DefaultProfile</span></span>
<span data-ttu-id="addb7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="addb7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="addb7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="addb7-115">-Name</span></span>
<span data-ttu-id="addb7-116">Name der Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="addb7-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="addb7-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="addb7-117">-RecurrenceInterval</span></span>
<span data-ttu-id="addb7-118">Das Wiederholungsintervall für die Synchronisierungseinstellung (Tag oder Stunde)</span><span class="sxs-lookup"><span data-stu-id="addb7-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="addb7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="addb7-119">-ResourceGroupName</span></span>
<span data-ttu-id="addb7-120">Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="addb7-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="addb7-121">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="addb7-121">-ShareName</span></span>
<span data-ttu-id="addb7-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="addb7-122">Azure data share name</span></span>

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

### <span data-ttu-id="addb7-123">-Synchronisierungs Zeitwahl</span><span class="sxs-lookup"><span data-stu-id="addb7-123">-SynchronizationTime</span></span>
<span data-ttu-id="addb7-124">Die Startzeit der Einstellung für die geplante Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="addb7-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="addb7-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="addb7-125">-Confirm</span></span>
<span data-ttu-id="addb7-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="addb7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="addb7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="addb7-127">-WhatIf</span></span>
<span data-ttu-id="addb7-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="addb7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="addb7-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="addb7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="addb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addb7-130">CommonParameters</span></span>
<span data-ttu-id="addb7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addb7-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="addb7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addb7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="addb7-133">INPUTS</span></span>

### <span data-ttu-id="addb7-134">Keine</span><span class="sxs-lookup"><span data-stu-id="addb7-134">None</span></span>

## <span data-ttu-id="addb7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="addb7-135">OUTPUTS</span></span>

### <span data-ttu-id="addb7-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="addb7-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="addb7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="addb7-137">NOTES</span></span>

## <span data-ttu-id="addb7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="addb7-138">RELATED LINKS</span></span>
