---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366930"
---
# <span data-ttu-id="a93d2-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="a93d2-101">Set-AzDataShare</span></span>

## <span data-ttu-id="a93d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a93d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a93d2-103">Aktualisiert eine vorhandene Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="a93d2-103">Updates an existing data share</span></span>

## <span data-ttu-id="a93d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a93d2-104">SYNTAX</span></span>

### <span data-ttu-id="a93d2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a93d2-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a93d2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a93d2-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a93d2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a93d2-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a93d2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a93d2-108">DESCRIPTION</span></span>
<span data-ttu-id="a93d2-109">Das **Cmdlet "Set-AzDataShare"** aktualisiert eine Datenfreigabe, die in einem angegebenen Azure Data Share-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a93d2-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="a93d2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a93d2-110">EXAMPLES</span></span>

### <span data-ttu-id="a93d2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a93d2-111">Example 1</span></span>
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

<span data-ttu-id="a93d2-112">Mit diesem Befehl wird eine vorhandene Datenfreigabe namens AdsShare aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a93d2-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="a93d2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a93d2-113">PARAMETERS</span></span>

### <span data-ttu-id="a93d2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a93d2-114">-AccountName</span></span>
<span data-ttu-id="a93d2-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="a93d2-115">Azure data share account name</span></span>

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

### <span data-ttu-id="a93d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93d2-116">-DefaultProfile</span></span>
<span data-ttu-id="a93d2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a93d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a93d2-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a93d2-118">-Description</span></span>
<span data-ttu-id="a93d2-119">Beschreibung der Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="a93d2-119">Description of Data Share</span></span>

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

### <span data-ttu-id="a93d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a93d2-120">-InputObject</span></span>
<span data-ttu-id="a93d2-121">Azure Data Share Object</span><span class="sxs-lookup"><span data-stu-id="a93d2-121">Azure data share object</span></span>


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

### <span data-ttu-id="a93d2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a93d2-122">-Name</span></span>
<span data-ttu-id="a93d2-123">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="a93d2-123">Azure data share name</span></span>

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

### <span data-ttu-id="a93d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a93d2-125">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="a93d2-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a93d2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a93d2-126">-ResourceId</span></span>
<span data-ttu-id="a93d2-127">Die Ressourcen-ID der Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="a93d2-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="a93d2-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="a93d2-128">-TermsOfUse</span></span>
<span data-ttu-id="a93d2-129">Nutzungsbedingungen für die Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="a93d2-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="a93d2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a93d2-130">-Confirm</span></span>
<span data-ttu-id="a93d2-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a93d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a93d2-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a93d2-132">-WhatIf</span></span>
<span data-ttu-id="a93d2-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a93d2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a93d2-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a93d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a93d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93d2-135">CommonParameters</span></span>
<span data-ttu-id="a93d2-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93d2-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a93d2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93d2-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a93d2-138">INPUTS</span></span>

### <span data-ttu-id="a93d2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a93d2-139">System.String</span></span>

### <span data-ttu-id="a93d2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="a93d2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="a93d2-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a93d2-141">OUTPUTS</span></span>

### <span data-ttu-id="a93d2-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="a93d2-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="a93d2-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a93d2-143">NOTES</span></span>

## <span data-ttu-id="a93d2-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a93d2-144">RELATED LINKS</span></span>
