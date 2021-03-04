---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: b3d0b292d7e680ca1d16e935c34a268cea836aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919171"
---
# <span data-ttu-id="b431b-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b431b-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b431b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b431b-102">SYNOPSIS</span></span>
<span data-ttu-id="b431b-103">Löscht einen Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="b431b-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b431b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b431b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b431b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b431b-105">DESCRIPTION</span></span>
<span data-ttu-id="b431b-106">Das **Cmdlet Remove-AzRecoveryServicesVault** löscht einen Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="b431b-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b431b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b431b-107">EXAMPLES</span></span>

### <span data-ttu-id="b431b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b431b-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="b431b-109">Löscht einen Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="b431b-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b431b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b431b-110">PARAMETERS</span></span>

### <span data-ttu-id="b431b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b431b-111">-DefaultProfile</span></span>
<span data-ttu-id="b431b-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b431b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b431b-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="b431b-113">-Vault</span></span>
<span data-ttu-id="b431b-114">Gibt ein Azure Site Recovery-Tresorobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b431b-114">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b431b-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b431b-115">-Confirm</span></span>
<span data-ttu-id="b431b-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b431b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b431b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b431b-117">-WhatIf</span></span>
<span data-ttu-id="b431b-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b431b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b431b-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b431b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b431b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b431b-120">CommonParameters</span></span>
<span data-ttu-id="b431b-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b431b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b431b-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b431b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b431b-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b431b-123">INPUTS</span></span>

### <span data-ttu-id="b431b-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="b431b-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b431b-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b431b-125">OUTPUTS</span></span>

### <span data-ttu-id="b431b-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="b431b-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="b431b-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b431b-127">NOTES</span></span>

## <span data-ttu-id="b431b-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b431b-128">RELATED LINKS</span></span>

[<span data-ttu-id="b431b-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b431b-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="b431b-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b431b-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b431b-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b431b-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


