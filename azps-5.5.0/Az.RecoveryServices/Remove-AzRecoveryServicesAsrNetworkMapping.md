---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156508"
---
# <span data-ttu-id="acdf0-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="acdf0-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="acdf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="acdf0-103">Löscht die angegebene ASR-Netzwerkzuordnung aus dem Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="acdf0-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="acdf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acdf0-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acdf0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="acdf0-105">DESCRIPTION</span></span>
<span data-ttu-id="acdf0-106">Das **Cmdlet "Remove-AzRecoveryServicesAsrNetworkMapping"** löscht die angegebene ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="acdf0-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="acdf0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="acdf0-107">EXAMPLES</span></span>

### <span data-ttu-id="acdf0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="acdf0-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="acdf0-109">Startet den Löschvorgang der angegebenen ASR-Netzwerkzuordnung und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="acdf0-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="acdf0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acdf0-110">PARAMETERS</span></span>

### <span data-ttu-id="acdf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdf0-111">-DefaultProfile</span></span>
<span data-ttu-id="acdf0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="acdf0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="acdf0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acdf0-113">-InputObject</span></span>
<span data-ttu-id="acdf0-114">Das Eingabeobjekt für das Cmdlet: Das ASR-Netzwerkzuordnungsobjekt, das der zu löschende ASR-Netzwerkzuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="acdf0-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acdf0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acdf0-115">-Confirm</span></span>
<span data-ttu-id="acdf0-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="acdf0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acdf0-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="acdf0-117">-WhatIf</span></span>
<span data-ttu-id="acdf0-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="acdf0-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acdf0-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="acdf0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acdf0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdf0-120">CommonParameters</span></span>
<span data-ttu-id="acdf0-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acdf0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdf0-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acdf0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdf0-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="acdf0-123">INPUTS</span></span>

### <span data-ttu-id="acdf0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="acdf0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="acdf0-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="acdf0-125">OUTPUTS</span></span>

### <span data-ttu-id="acdf0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="acdf0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="acdf0-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="acdf0-127">NOTES</span></span>

## <span data-ttu-id="acdf0-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="acdf0-128">RELATED LINKS</span></span>

[<span data-ttu-id="acdf0-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="acdf0-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="acdf0-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="acdf0-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
