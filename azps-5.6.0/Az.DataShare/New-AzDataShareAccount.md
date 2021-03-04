---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: 91f6c56849d5b8ca96af2a28191cefde803f63c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935787"
---
# <span data-ttu-id="5a64a-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="5a64a-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="5a64a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a64a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a64a-103">Erstellt ein neues Datenfreigabekonto</span><span class="sxs-lookup"><span data-stu-id="5a64a-103">Creates new data share account</span></span>

## <span data-ttu-id="5a64a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a64a-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a64a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a64a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a64a-106">**Das Cmdlet New-AzDataShareAccount** erstellt ein Datenfreigabekonto in der angegebenen Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a64a-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="5a64a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a64a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a64a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a64a-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="5a64a-109">Erstellt ein Konto mit dem Namen "WikiADS" in der Ressourcengruppe "ADS"</span><span class="sxs-lookup"><span data-stu-id="5a64a-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="5a64a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5a64a-110">PARAMETERS</span></span>

### <span data-ttu-id="5a64a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a64a-111">-AsJob</span></span>
<span data-ttu-id="5a64a-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="5a64a-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="5a64a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a64a-113">-DefaultProfile</span></span>
<span data-ttu-id="5a64a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a64a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a64a-115">-Location</span><span class="sxs-lookup"><span data-stu-id="5a64a-115">-Location</span></span>
<span data-ttu-id="5a64a-116">Der Speicherort, an dem das Datenfreigabekonto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a64a-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="5a64a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5a64a-117">-Name</span></span>
<span data-ttu-id="5a64a-118">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="5a64a-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="5a64a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a64a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a64a-120">Der Ressourcengruppenname des Azure Data Share-Kontos wird in erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a64a-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="5a64a-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a64a-121">-Tag</span></span>
<span data-ttu-id="5a64a-122">Die Tags, die dem Azure Data Share-Konto zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5a64a-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a64a-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a64a-123">-Confirm</span></span>
<span data-ttu-id="5a64a-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a64a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a64a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a64a-125">-WhatIf</span></span>
<span data-ttu-id="5a64a-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a64a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a64a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a64a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a64a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a64a-128">CommonParameters</span></span>
<span data-ttu-id="5a64a-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a64a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a64a-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a64a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a64a-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a64a-131">INPUTS</span></span>

### <span data-ttu-id="5a64a-132">Keine</span><span class="sxs-lookup"><span data-stu-id="5a64a-132">None</span></span>

## <span data-ttu-id="5a64a-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a64a-133">OUTPUTS</span></span>

### <span data-ttu-id="5a64a-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="5a64a-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="5a64a-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5a64a-135">NOTES</span></span>

## <span data-ttu-id="5a64a-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5a64a-136">RELATED LINKS</span></span>
