---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151124"
---
# <span data-ttu-id="2fc9e-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2fc9e-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="2fc9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc9e-103">Deletes the specified Protection Container from its Fabric.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="2fc9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fc9e-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc9e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fc9e-105">DESCRIPTION</span></span>
<span data-ttu-id="2fc9e-106">Das Remove-AzRecoveryServicesAsrProtectionContainer cmdlet löscht den angegebenen Azure Site Recovery Protection-Container.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="2fc9e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fc9e-107">EXAMPLES</span></span>

### <span data-ttu-id="2fc9e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fc9e-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="2fc9e-109">Startet das Löschen des angegebenen Schutzcontainers und gibt den ASR-Auftrag zurück, mit dem der Entfernungsvorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="2fc9e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fc9e-110">PARAMETERS</span></span>

### <span data-ttu-id="2fc9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc9e-111">-DefaultProfile</span></span>
<span data-ttu-id="2fc9e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc9e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fc9e-113">-InputObject</span></span>
<span data-ttu-id="2fc9e-114">Gibt den Schutzcontainer an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="2fc9e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fc9e-115">-Confirm</span></span>
<span data-ttu-id="2fc9e-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc9e-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2fc9e-117">-WhatIf</span></span>
<span data-ttu-id="2fc9e-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc9e-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc9e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc9e-120">CommonParameters</span></span>
<span data-ttu-id="2fc9e-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc9e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc9e-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fc9e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc9e-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fc9e-123">INPUTS</span></span>

### <span data-ttu-id="2fc9e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2fc9e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="2fc9e-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fc9e-125">OUTPUTS</span></span>

### <span data-ttu-id="2fc9e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="2fc9e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2fc9e-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2fc9e-127">NOTES</span></span>

## <span data-ttu-id="2fc9e-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2fc9e-128">RELATED LINKS</span></span>
