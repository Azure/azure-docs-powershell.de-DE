---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153337"
---
# <span data-ttu-id="00d6e-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="00d6e-101">New-AzDataShare</span></span>

## <span data-ttu-id="00d6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="00d6e-103">Erstellt eine Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="00d6e-103">Creates a azure data share.</span></span>

## <span data-ttu-id="00d6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00d6e-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00d6e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00d6e-105">DESCRIPTION</span></span>
<span data-ttu-id="00d6e-106">Das **Cmdlet "New-AzDataShare"** erstellt eine Datenfreigabe innerhalb eines angegebenen Azure Data Share-Kontos, indem der Name der Ressourcengruppe, der Kontoname, der Freigabename und die Freigabetyp angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="00d6e-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="00d6e-107">Beschreibung und Nutzungsbedingungen sind optionale Parameter, die beim Erstellen der Datenfreigabe festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="00d6e-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="00d6e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00d6e-108">EXAMPLES</span></span>

### <span data-ttu-id="00d6e-109">Beispiel 1: Erstellen einer Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="00d6e-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="00d6e-110">Mit diesem Befehl wird eine Datenfreigabe mit dem Namen "AdsShare of kind CopyBased" im Datenfreigabekonto "WikiAdsAccount" unter der Ressourcengruppe ADS mit einer Beschreibung und Nutzungsbedingungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="00d6e-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="00d6e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00d6e-111">PARAMETERS</span></span>

### <span data-ttu-id="00d6e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="00d6e-112">-AccountName</span></span>
<span data-ttu-id="00d6e-113">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="00d6e-113">Azure data share account name</span></span>

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

### <span data-ttu-id="00d6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d6e-114">-DefaultProfile</span></span>
<span data-ttu-id="00d6e-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00d6e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00d6e-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00d6e-116">-Description</span></span>
<span data-ttu-id="00d6e-117">Beschreibung der Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="00d6e-117">Description of azure data share</span></span>

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

### <span data-ttu-id="00d6e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="00d6e-118">-Name</span></span>
<span data-ttu-id="00d6e-119">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="00d6e-119">Azure data share name</span></span>

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

### <span data-ttu-id="00d6e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00d6e-120">-ResourceGroupName</span></span>
<span data-ttu-id="00d6e-121">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="00d6e-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="00d6e-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="00d6e-122">-TermsOfUse</span></span>
<span data-ttu-id="00d6e-123">Nutzungsbedingungen für die Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="00d6e-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="00d6e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00d6e-124">-Confirm</span></span>
<span data-ttu-id="00d6e-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00d6e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00d6e-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="00d6e-126">-WhatIf</span></span>
<span data-ttu-id="00d6e-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00d6e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00d6e-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00d6e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00d6e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d6e-129">CommonParameters</span></span>
<span data-ttu-id="00d6e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d6e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d6e-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00d6e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d6e-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00d6e-132">INPUTS</span></span>

### <span data-ttu-id="00d6e-133">Keine</span><span class="sxs-lookup"><span data-stu-id="00d6e-133">None</span></span>

## <span data-ttu-id="00d6e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00d6e-134">OUTPUTS</span></span>

### <span data-ttu-id="00d6e-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="00d6e-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="00d6e-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="00d6e-136">NOTES</span></span>

## <span data-ttu-id="00d6e-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="00d6e-137">RELATED LINKS</span></span>
