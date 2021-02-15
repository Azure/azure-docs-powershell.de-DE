---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160089"
---
# <span data-ttu-id="a3f63-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a3f63-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a3f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3f63-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f63-103">Löscht einen Wiederherstellungsdienste-Tresor.</span><span class="sxs-lookup"><span data-stu-id="a3f63-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a3f63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3f63-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3f63-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3f63-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f63-106">Das **Cmdlet "Remove-AzRecoveryServicesVault"** löscht einen Wiederherstellungsdienst-Tresor.</span><span class="sxs-lookup"><span data-stu-id="a3f63-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a3f63-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3f63-107">EXAMPLES</span></span>

### <span data-ttu-id="a3f63-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3f63-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="a3f63-109">Löscht einen Wiederherstellungsdienste-Tresor.</span><span class="sxs-lookup"><span data-stu-id="a3f63-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a3f63-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3f63-110">PARAMETERS</span></span>

### <span data-ttu-id="a3f63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f63-111">-DefaultProfile</span></span>
<span data-ttu-id="a3f63-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3f63-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f63-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="a3f63-113">-Vault</span></span>
<span data-ttu-id="a3f63-114">Gibt ein Azure Site Recovery -Tresorobjekt an.</span><span class="sxs-lookup"><span data-stu-id="a3f63-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="a3f63-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3f63-115">-Confirm</span></span>
<span data-ttu-id="a3f63-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3f63-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3f63-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a3f63-117">-WhatIf</span></span>
<span data-ttu-id="a3f63-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3f63-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3f63-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3f63-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3f63-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f63-120">CommonParameters</span></span>
<span data-ttu-id="a3f63-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f63-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f63-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3f63-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f63-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3f63-123">INPUTS</span></span>

### <span data-ttu-id="a3f63-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="a3f63-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a3f63-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3f63-125">OUTPUTS</span></span>

### <span data-ttu-id="a3f63-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="a3f63-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="a3f63-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3f63-127">NOTES</span></span>

## <span data-ttu-id="a3f63-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3f63-128">RELATED LINKS</span></span>

[<span data-ttu-id="a3f63-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a3f63-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="a3f63-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a3f63-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a3f63-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a3f63-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


