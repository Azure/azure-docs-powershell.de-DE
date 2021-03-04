---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: cda809b8c6c4425a3df7bd4ba5ae40a9292e358f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942787"
---
# <span data-ttu-id="256ff-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="256ff-101">New-AzDataShare</span></span>

## <span data-ttu-id="256ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="256ff-102">SYNOPSIS</span></span>
<span data-ttu-id="256ff-103">Erstellt eine Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="256ff-103">Creates a azure data share.</span></span>

## <span data-ttu-id="256ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="256ff-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="256ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="256ff-105">DESCRIPTION</span></span>
<span data-ttu-id="256ff-106">Das **New-AzDataShare-Cmdlet** erstellt eine Datenfreigabe innerhalb eines angegebenen Azure-Datenfreigabekontos, indem der Ressourcengruppenname, kontoname, Freigabename und Freigabetyp angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="256ff-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="256ff-107">Beschreibung und Nutzungsbedingungen sind optionale Parameter, die beim Erstellen der Datenfreigabe festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="256ff-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="256ff-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="256ff-108">EXAMPLES</span></span>

### <span data-ttu-id="256ff-109">Beispiel 1: Erstellen einer Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="256ff-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="256ff-110">Mit diesem Befehl wird eine Datenfreigabe mit dem Namen AdsShare der Art CopyBased im WikiAdsAccount für Datenfreigaben unter der Ressourcengruppe ADS mit Beschreibung und Nutzungsbedingungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="256ff-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="256ff-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="256ff-111">PARAMETERS</span></span>

### <span data-ttu-id="256ff-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="256ff-112">-AccountName</span></span>
<span data-ttu-id="256ff-113">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="256ff-113">Azure data share account name</span></span>

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

### <span data-ttu-id="256ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="256ff-114">-DefaultProfile</span></span>
<span data-ttu-id="256ff-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="256ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="256ff-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="256ff-116">-Description</span></span>
<span data-ttu-id="256ff-117">Beschreibung der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="256ff-117">Description of azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256ff-118">-Name</span><span class="sxs-lookup"><span data-stu-id="256ff-118">-Name</span></span>
<span data-ttu-id="256ff-119">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="256ff-119">Azure data share name</span></span>

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

### <span data-ttu-id="256ff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="256ff-120">-ResourceGroupName</span></span>
<span data-ttu-id="256ff-121">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="256ff-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="256ff-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="256ff-122">-TermsOfUse</span></span>
<span data-ttu-id="256ff-123">Nutzungsbedingungen für azure data share</span><span class="sxs-lookup"><span data-stu-id="256ff-123">Terms of use for azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256ff-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="256ff-124">-Confirm</span></span>
<span data-ttu-id="256ff-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="256ff-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="256ff-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="256ff-126">-WhatIf</span></span>
<span data-ttu-id="256ff-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="256ff-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="256ff-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="256ff-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="256ff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256ff-129">CommonParameters</span></span>
<span data-ttu-id="256ff-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="256ff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256ff-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="256ff-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256ff-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="256ff-132">INPUTS</span></span>

### <span data-ttu-id="256ff-133">Keine</span><span class="sxs-lookup"><span data-stu-id="256ff-133">None</span></span>

## <span data-ttu-id="256ff-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="256ff-134">OUTPUTS</span></span>

### <span data-ttu-id="256ff-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="256ff-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="256ff-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="256ff-136">NOTES</span></span>

## <span data-ttu-id="256ff-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="256ff-137">RELATED LINKS</span></span>
