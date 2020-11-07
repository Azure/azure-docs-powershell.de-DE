---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 9dca6272991c67375f2764725901018c331e0ca9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651423"
---
# <span data-ttu-id="20324-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="20324-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="20324-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20324-102">SYNOPSIS</span></span>
<span data-ttu-id="20324-103">Ruft Informationen zur Synchronisierungseinstellung für eine Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="20324-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="20324-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20324-104">SYNTAX</span></span>

### <span data-ttu-id="20324-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="20324-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20324-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20324-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20324-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20324-107">DESCRIPTION</span></span>
<span data-ttu-id="20324-108">Das Cmdlet " **Get-AzDataShareSynchronizationSetting** " enthält Informationen über die Synchronisierung, die für eine Freigabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="20324-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="20324-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20324-109">EXAMPLES</span></span>

### <span data-ttu-id="20324-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20324-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="20324-111">Dieser Befehl bietet Informationen zu Synchronisierungs ShareSynchronization, die für Freigabe AdsShare unter Datenfreigabe Konto WikiAds aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="20324-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="20324-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="20324-112">PARAMETERS</span></span>

### <span data-ttu-id="20324-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="20324-113">-AccountName</span></span>
<span data-ttu-id="20324-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="20324-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20324-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20324-115">-DefaultProfile</span></span>
<span data-ttu-id="20324-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20324-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20324-117">-Name</span><span class="sxs-lookup"><span data-stu-id="20324-117">-Name</span></span>
<span data-ttu-id="20324-118">Name für Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="20324-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20324-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20324-119">-ResourceGroupName</span></span>
<span data-ttu-id="20324-120">Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="20324-120">Resource group name of azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20324-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="20324-121">-ResourceId</span></span>
<span data-ttu-id="20324-122">Die Ressourcen-ID der Azure Data Share-Synchronisierungseinstellung</span><span class="sxs-lookup"><span data-stu-id="20324-122">The resource id of the azure data share synchronization setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20324-123">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="20324-123">-ShareName</span></span>
<span data-ttu-id="20324-124">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="20324-124">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20324-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20324-125">CommonParameters</span></span>
<span data-ttu-id="20324-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20324-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20324-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20324-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20324-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20324-128">INPUTS</span></span>

### <span data-ttu-id="20324-129">System. String</span><span class="sxs-lookup"><span data-stu-id="20324-129">System.String</span></span>

## <span data-ttu-id="20324-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20324-130">OUTPUTS</span></span>

### <span data-ttu-id="20324-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="20324-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="20324-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="20324-132">NOTES</span></span>

## <span data-ttu-id="20324-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20324-133">RELATED LINKS</span></span>
