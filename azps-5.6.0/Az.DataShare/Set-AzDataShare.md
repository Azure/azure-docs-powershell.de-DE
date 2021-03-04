---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: ea159b52de0dd7d30c898f5119bc819c94d418fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925875"
---
# <span data-ttu-id="3deb6-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="3deb6-101">Set-AzDataShare</span></span>

## <span data-ttu-id="3deb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3deb6-102">SYNOPSIS</span></span>
<span data-ttu-id="3deb6-103">Aktualisiert eine vorhandene Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="3deb6-103">Updates an existing data share</span></span>

## <span data-ttu-id="3deb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3deb6-104">SYNTAX</span></span>

### <span data-ttu-id="3deb6-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3deb6-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3deb6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3deb6-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3deb6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3deb6-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3deb6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3deb6-108">DESCRIPTION</span></span>
<span data-ttu-id="3deb6-109">Das **Set-AzDataShare-Cmdlet** aktualisiert eine Datenfreigabe, die in einem angegebenen Azure Data Share-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3deb6-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="3deb6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3deb6-110">EXAMPLES</span></span>

### <span data-ttu-id="3deb6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3deb6-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="3deb6-112">Mit diesem Befehl wird eine vorhandene Datenfreigabe namens AdsShare aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3deb6-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="3deb6-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3deb6-113">PARAMETERS</span></span>

### <span data-ttu-id="3deb6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3deb6-114">-AccountName</span></span>
<span data-ttu-id="3deb6-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="3deb6-115">Azure data share account name</span></span>

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

### <span data-ttu-id="3deb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3deb6-116">-DefaultProfile</span></span>
<span data-ttu-id="3deb6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3deb6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3deb6-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3deb6-118">-Description</span></span>
<span data-ttu-id="3deb6-119">Beschreibung der Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="3deb6-119">Description of Data Share</span></span>

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

### <span data-ttu-id="3deb6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3deb6-120">-InputObject</span></span>
<span data-ttu-id="3deb6-121">Azure-Datenfreigabeobjekt</span><span class="sxs-lookup"><span data-stu-id="3deb6-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3deb6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3deb6-122">-Name</span></span>
<span data-ttu-id="3deb6-123">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="3deb6-123">Azure data share name</span></span>

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

### <span data-ttu-id="3deb6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3deb6-124">-ResourceGroupName</span></span>
<span data-ttu-id="3deb6-125">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="3deb6-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3deb6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3deb6-126">-ResourceId</span></span>
<span data-ttu-id="3deb6-127">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="3deb6-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="3deb6-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="3deb6-128">-TermsOfUse</span></span>
<span data-ttu-id="3deb6-129">Nutzungsbedingungen für die Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="3deb6-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="3deb6-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3deb6-130">-Confirm</span></span>
<span data-ttu-id="3deb6-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3deb6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3deb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3deb6-132">-WhatIf</span></span>
<span data-ttu-id="3deb6-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3deb6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3deb6-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3deb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3deb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3deb6-135">CommonParameters</span></span>
<span data-ttu-id="3deb6-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3deb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3deb6-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3deb6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3deb6-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3deb6-138">INPUTS</span></span>

### <span data-ttu-id="3deb6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3deb6-139">System.String</span></span>

### <span data-ttu-id="3deb6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="3deb6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="3deb6-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3deb6-141">OUTPUTS</span></span>

### <span data-ttu-id="3deb6-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="3deb6-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="3deb6-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3deb6-143">NOTES</span></span>

## <span data-ttu-id="3deb6-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3deb6-144">RELATED LINKS</span></span>
