---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297441"
---
# <span data-ttu-id="360d2-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="360d2-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="360d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="360d2-102">SYNOPSIS</span></span>
<span data-ttu-id="360d2-103">Erstellt eine Einladung zur Freigabe.</span><span class="sxs-lookup"><span data-stu-id="360d2-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="360d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="360d2-104">SYNTAX</span></span>

### <span data-ttu-id="360d2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="360d2-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="360d2-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="360d2-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="360d2-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="360d2-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="360d2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="360d2-108">DESCRIPTION</span></span>
<span data-ttu-id="360d2-109">Das Cmdlet **New-AzDataShareInvitation** sendet eine Einladung an den Zielbenutzer mit Informationen zur Anbieter Freigabe.</span><span class="sxs-lookup"><span data-stu-id="360d2-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="360d2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="360d2-110">EXAMPLES</span></span>

### <span data-ttu-id="360d2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="360d2-111">Example 1</span></span>
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

<span data-ttu-id="360d2-112">Dieser Befehl erstellt eine Einladungs-AdsInvitation für Freigabe-AdsShare und sendet Sie an eine Ziel-e-Mail adstest@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="360d2-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="360d2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="360d2-113">PARAMETERS</span></span>

### <span data-ttu-id="360d2-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="360d2-114">-AccountName</span></span>
<span data-ttu-id="360d2-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="360d2-115">Azure data share account name</span></span>

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

### <span data-ttu-id="360d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360d2-116">-DefaultProfile</span></span>
<span data-ttu-id="360d2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="360d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="360d2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="360d2-118">-Name</span></span>
<span data-ttu-id="360d2-119">Name der Einladung zu Azure Data Freigabe</span><span class="sxs-lookup"><span data-stu-id="360d2-119">Azure data share invitation name</span></span>

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

### <span data-ttu-id="360d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="360d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="360d2-121">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="360d2-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="360d2-122">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="360d2-122">-ShareName</span></span>
<span data-ttu-id="360d2-123">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="360d2-123">Azure data share name</span></span>

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

### <span data-ttu-id="360d2-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="360d2-124">-TargetEmail</span></span>
<span data-ttu-id="360d2-125">Ziel-e-Mail-ID</span><span class="sxs-lookup"><span data-stu-id="360d2-125">Target email id</span></span>

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

### <span data-ttu-id="360d2-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="360d2-126">-TargetObjectId</span></span>
<span data-ttu-id="360d2-127">Zielobjekt-ID</span><span class="sxs-lookup"><span data-stu-id="360d2-127">Target object id</span></span>

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

### <span data-ttu-id="360d2-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="360d2-128">-TargetTenantId</span></span>
<span data-ttu-id="360d2-129">Zielmandanten-ID</span><span class="sxs-lookup"><span data-stu-id="360d2-129">Target tenant id</span></span>

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

### <span data-ttu-id="360d2-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="360d2-130">-Confirm</span></span>
<span data-ttu-id="360d2-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="360d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="360d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360d2-132">-WhatIf</span></span>
<span data-ttu-id="360d2-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="360d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="360d2-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="360d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="360d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360d2-135">CommonParameters</span></span>
<span data-ttu-id="360d2-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360d2-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="360d2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360d2-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="360d2-138">INPUTS</span></span>

### <span data-ttu-id="360d2-139">Keine</span><span class="sxs-lookup"><span data-stu-id="360d2-139">None</span></span>

## <span data-ttu-id="360d2-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="360d2-140">OUTPUTS</span></span>

### <span data-ttu-id="360d2-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="360d2-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="360d2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="360d2-142">NOTES</span></span>

## <span data-ttu-id="360d2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="360d2-143">RELATED LINKS</span></span>
