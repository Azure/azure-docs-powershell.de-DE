---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: c1b5623e185c10471da674c21995917c169e5ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919243"
---
# <span data-ttu-id="d55dd-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d55dd-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d55dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d55dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d55dd-103">Löscht den angegebenen Schutzcontainer aus seinem Fabric.</span><span class="sxs-lookup"><span data-stu-id="d55dd-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="d55dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d55dd-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d55dd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d55dd-105">DESCRIPTION</span></span>
<span data-ttu-id="d55dd-106">Das Remove-AzRecoveryServicesAsrProtectionContainer-Cmdlet löscht den angegebenen Azure Site Recovery Protection-Container.</span><span class="sxs-lookup"><span data-stu-id="d55dd-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d55dd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d55dd-107">EXAMPLES</span></span>

### <span data-ttu-id="d55dd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d55dd-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="d55dd-109">Startet das Löschen des angegebenen Schutzcontainers und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Entfernungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d55dd-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="d55dd-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d55dd-110">PARAMETERS</span></span>

### <span data-ttu-id="d55dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55dd-111">-DefaultProfile</span></span>
<span data-ttu-id="d55dd-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d55dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d55dd-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d55dd-113">-InputObject</span></span>
<span data-ttu-id="d55dd-114">Gibt den zu entfernenden Schutzcontainer an.</span><span class="sxs-lookup"><span data-stu-id="d55dd-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d55dd-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d55dd-115">-Confirm</span></span>
<span data-ttu-id="d55dd-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d55dd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d55dd-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d55dd-117">-WhatIf</span></span>
<span data-ttu-id="d55dd-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d55dd-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d55dd-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d55dd-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d55dd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55dd-120">CommonParameters</span></span>
<span data-ttu-id="d55dd-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55dd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55dd-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d55dd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55dd-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d55dd-123">INPUTS</span></span>

### <span data-ttu-id="d55dd-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d55dd-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d55dd-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d55dd-125">OUTPUTS</span></span>

### <span data-ttu-id="d55dd-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d55dd-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d55dd-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d55dd-127">NOTES</span></span>

## <span data-ttu-id="d55dd-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d55dd-128">RELATED LINKS</span></span>
