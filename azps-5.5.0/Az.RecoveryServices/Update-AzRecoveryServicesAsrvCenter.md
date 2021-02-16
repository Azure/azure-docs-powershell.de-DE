---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151060"
---
# <span data-ttu-id="9422b-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="9422b-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="9422b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9422b-102">SYNOPSIS</span></span>
<span data-ttu-id="9422b-103">Aktualisieren von Discoverydetails für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="9422b-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9422b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9422b-104">SYNTAX</span></span>

### <span data-ttu-id="9422b-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="9422b-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9422b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9422b-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9422b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9422b-107">DESCRIPTION</span></span>
<span data-ttu-id="9422b-108">Das **Cmdlet "Update-AzRecoveryServicesAsrvCenter"** aktualisiert Discoverydetails für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="9422b-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9422b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9422b-109">EXAMPLES</span></span>

### <span data-ttu-id="9422b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9422b-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="9422b-111">Aktualisieren von Discoverydetails für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="9422b-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9422b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9422b-112">PARAMETERS</span></span>

### <span data-ttu-id="9422b-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="9422b-113">-Account</span></span>
<span data-ttu-id="9422b-114">vCenter-Anmeldeinformationen-Konto.</span><span class="sxs-lookup"><span data-stu-id="9422b-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9422b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9422b-115">-DefaultProfile</span></span>
<span data-ttu-id="9422b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9422b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9422b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9422b-117">-InputObject</span></span>
<span data-ttu-id="9422b-118">Das vCenter-Serverobjekt, für das Discoverydetails aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9422b-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9422b-119">-Port</span><span class="sxs-lookup"><span data-stu-id="9422b-119">-Port</span></span>
<span data-ttu-id="9422b-120">Der TCP-Port auf dem vCenter-Server, der für die Ermittlung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9422b-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9422b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9422b-121">-ResourceId</span></span>
<span data-ttu-id="9422b-122">Gibt die resourceId von vCenter an.</span><span class="sxs-lookup"><span data-stu-id="9422b-122">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9422b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9422b-123">-Confirm</span></span>
<span data-ttu-id="9422b-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9422b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9422b-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9422b-125">-WhatIf</span></span>
<span data-ttu-id="9422b-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9422b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9422b-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9422b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9422b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9422b-128">CommonParameters</span></span>
<span data-ttu-id="9422b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9422b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9422b-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9422b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9422b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9422b-131">INPUTS</span></span>

### <span data-ttu-id="9422b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9422b-132">System.String</span></span>

### <span data-ttu-id="9422b-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="9422b-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="9422b-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9422b-134">OUTPUTS</span></span>

### <span data-ttu-id="9422b-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9422b-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9422b-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9422b-136">NOTES</span></span>

## <span data-ttu-id="9422b-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9422b-137">RELATED LINKS</span></span>
