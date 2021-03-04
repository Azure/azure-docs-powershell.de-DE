---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: 4892e5e31c67725d15af7be015ca27bd450babd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946079"
---
# <span data-ttu-id="07e01-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="07e01-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="07e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07e01-102">SYNOPSIS</span></span>
<span data-ttu-id="07e01-103">Regeneriert einen Kontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="07e01-103">Regenerates an account key.</span></span>

## <span data-ttu-id="07e01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07e01-104">SYNTAX</span></span>

### <span data-ttu-id="07e01-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07e01-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07e01-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07e01-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07e01-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07e01-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07e01-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07e01-108">DESCRIPTION</span></span>
<span data-ttu-id="07e01-109">Das New-AzMapsAccountKey cmdlet generiert einen API-Schlüssel für ein Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="07e01-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="07e01-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07e01-110">EXAMPLES</span></span>

### <span data-ttu-id="07e01-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07e01-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="07e01-112">Regeneriert den primären API-Schlüssel für das Konto MyAccount in der Ressourcengruppe MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="07e01-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="07e01-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="07e01-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="07e01-114">Regeneriert den sekundären API-Schlüssel für das angegebene Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="07e01-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="07e01-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="07e01-115">PARAMETERS</span></span>

### <span data-ttu-id="07e01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e01-116">-DefaultProfile</span></span>
<span data-ttu-id="07e01-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07e01-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07e01-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07e01-118">-InputObject</span></span>
<span data-ttu-id="07e01-119">Kartenkonto aus Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="07e01-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07e01-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="07e01-120">-KeyName</span></span>
<span data-ttu-id="07e01-121">Karten-Kontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="07e01-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e01-122">-Name</span><span class="sxs-lookup"><span data-stu-id="07e01-122">-Name</span></span>
<span data-ttu-id="07e01-123">Karten-Kontoname.</span><span class="sxs-lookup"><span data-stu-id="07e01-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e01-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e01-124">-ResourceGroupName</span></span>
<span data-ttu-id="07e01-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="07e01-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e01-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07e01-126">-ResourceId</span></span>
<span data-ttu-id="07e01-127">Ordnet "Account ResourceId" zu.</span><span class="sxs-lookup"><span data-stu-id="07e01-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e01-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07e01-128">-Confirm</span></span>
<span data-ttu-id="07e01-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07e01-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07e01-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07e01-130">-WhatIf</span></span>
<span data-ttu-id="07e01-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07e01-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07e01-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07e01-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07e01-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e01-133">CommonParameters</span></span>
<span data-ttu-id="07e01-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e01-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e01-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e01-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e01-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07e01-136">INPUTS</span></span>

### <span data-ttu-id="07e01-137">System.String</span><span class="sxs-lookup"><span data-stu-id="07e01-137">System.String</span></span>

### <span data-ttu-id="07e01-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="07e01-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="07e01-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07e01-139">OUTPUTS</span></span>

### <span data-ttu-id="07e01-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="07e01-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="07e01-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="07e01-141">NOTES</span></span>

## <span data-ttu-id="07e01-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="07e01-142">RELATED LINKS</span></span>
