---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4e0b74ead08a3b944e66b46a6fee0fb71976b223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929435"
---
# <span data-ttu-id="85591-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="85591-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="85591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85591-102">SYNOPSIS</span></span>
<span data-ttu-id="85591-103">Gibt die Eigenschaften eines Wiederherstellungsdienste-Tresors zurück.</span><span class="sxs-lookup"><span data-stu-id="85591-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="85591-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85591-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85591-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85591-105">DESCRIPTION</span></span>
<span data-ttu-id="85591-106">Das **Get-AzRecoveryServicesVaultProperty-Cmdlet** gibt die Eigenschaften eines Wiederherstellungsdiensttresor zurück.</span><span class="sxs-lookup"><span data-stu-id="85591-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="85591-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85591-107">EXAMPLES</span></span>

### <span data-ttu-id="85591-108">Beispiel 1: Erhalten von Eigenschaften eines Tresors</span><span class="sxs-lookup"><span data-stu-id="85591-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="85591-109">Der erste Befehl ruft ein Tresorobjekt ab und speichert es dann in der $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="85591-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="85591-110">Der zweite Befehl ruft die Tresoreigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="85591-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="85591-111">Als Nächstes greifen wir auf die VerschlüsselungProperties des Tresors zu.</span><span class="sxs-lookup"><span data-stu-id="85591-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="85591-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="85591-112">PARAMETERS</span></span>

### <span data-ttu-id="85591-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85591-113">-DefaultProfile</span></span>
<span data-ttu-id="85591-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85591-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85591-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="85591-115">-VaultId</span></span>
<span data-ttu-id="85591-116">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="85591-116">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85591-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85591-117">CommonParameters</span></span>
<span data-ttu-id="85591-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85591-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85591-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85591-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85591-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85591-120">INPUTS</span></span>

### <span data-ttu-id="85591-121">System.String</span><span class="sxs-lookup"><span data-stu-id="85591-121">System.String</span></span>

## <span data-ttu-id="85591-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85591-122">OUTPUTS</span></span>

### <span data-ttu-id="85591-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="85591-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="85591-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="85591-124">NOTES</span></span>

## <span data-ttu-id="85591-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="85591-125">RELATED LINKS</span></span>

[<span data-ttu-id="85591-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="85591-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="85591-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="85591-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
