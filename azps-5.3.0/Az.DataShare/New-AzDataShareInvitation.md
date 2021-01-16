---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377235"
---
# <span data-ttu-id="07e9f-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="07e9f-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="07e9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="07e9f-103">Erstellt eine Einladung zur Freigabe.</span><span class="sxs-lookup"><span data-stu-id="07e9f-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="07e9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07e9f-104">SYNTAX</span></span>

### <span data-ttu-id="07e9f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07e9f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07e9f-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="07e9f-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07e9f-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="07e9f-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07e9f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07e9f-108">DESCRIPTION</span></span>
<span data-ttu-id="07e9f-109">Das **Cmdlet "New-AzDataShareInvitation"** sendet eine Einladung mit Informationen zur Anbieterfreigabe an den Zielverbraucher.</span><span class="sxs-lookup"><span data-stu-id="07e9f-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="07e9f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07e9f-110">EXAMPLES</span></span>

### <span data-ttu-id="07e9f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07e9f-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="07e9f-112">Mit diesem Befehl wird eine Einladung zu AdsInvitation zum Teilen von AdsShare erstellt und an die Ziel-E-Mail adstest@microsoft.com gesendet.</span><span class="sxs-lookup"><span data-stu-id="07e9f-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="07e9f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07e9f-113">PARAMETERS</span></span>

### <span data-ttu-id="07e9f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="07e9f-114">-AccountName</span></span>
<span data-ttu-id="07e9f-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="07e9f-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e9f-116">-DefaultProfile</span></span>
<span data-ttu-id="07e9f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07e9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07e9f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="07e9f-118">-Name</span></span>
<span data-ttu-id="07e9f-119">Name der Einladung zur Freigabe von Azure-Daten</span><span class="sxs-lookup"><span data-stu-id="07e9f-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e9f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e9f-120">-ResourceGroupName</span></span>
<span data-ttu-id="07e9f-121">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="07e9f-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e9f-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="07e9f-122">-ShareName</span></span>
<span data-ttu-id="07e9f-123">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="07e9f-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e9f-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="07e9f-124">-TargetEmail</span></span>
<span data-ttu-id="07e9f-125">Ziel-E-Mail-ID</span><span class="sxs-lookup"><span data-stu-id="07e9f-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e9f-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="07e9f-126">-TargetObjectId</span></span>
<span data-ttu-id="07e9f-127">Zielobjekt-ID</span><span class="sxs-lookup"><span data-stu-id="07e9f-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e9f-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="07e9f-128">-TargetTenantId</span></span>
<span data-ttu-id="07e9f-129">Ziel-Mandant-ID</span><span class="sxs-lookup"><span data-stu-id="07e9f-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e9f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07e9f-130">-Confirm</span></span>
<span data-ttu-id="07e9f-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07e9f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07e9f-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="07e9f-132">-WhatIf</span></span>
<span data-ttu-id="07e9f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07e9f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07e9f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07e9f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07e9f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e9f-135">CommonParameters</span></span>
<span data-ttu-id="07e9f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e9f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e9f-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07e9f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e9f-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07e9f-138">INPUTS</span></span>

### <span data-ttu-id="07e9f-139">Keine</span><span class="sxs-lookup"><span data-stu-id="07e9f-139">None</span></span>

## <span data-ttu-id="07e9f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07e9f-140">OUTPUTS</span></span>

### <span data-ttu-id="07e9f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="07e9f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="07e9f-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07e9f-142">NOTES</span></span>

## <span data-ttu-id="07e9f-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07e9f-143">RELATED LINKS</span></span>
