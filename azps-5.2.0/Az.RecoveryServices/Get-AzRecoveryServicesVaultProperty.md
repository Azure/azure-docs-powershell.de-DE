---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296632"
---
# <span data-ttu-id="04f0e-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="04f0e-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="04f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="04f0e-103">Gibt die Eigenschaften eines Wiederherstellungsdiensttresor zurück.</span><span class="sxs-lookup"><span data-stu-id="04f0e-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="04f0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04f0e-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04f0e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="04f0e-106">Das **Cmdlet "Get-AzRecoveryServicesVaultProperty"** gibt die Eigenschaften eines Tresors für Wiederherstellungsdienste zurück.</span><span class="sxs-lookup"><span data-stu-id="04f0e-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="04f0e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04f0e-107">EXAMPLES</span></span>

### <span data-ttu-id="04f0e-108">Beispiel 1: Erhalten der Eigenschaften eines Tresors</span><span class="sxs-lookup"><span data-stu-id="04f0e-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="04f0e-109">Der erste Befehl ruft ein Tresorobjekt ab und speichert es dann in der $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="04f0e-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="04f0e-110">Der zweite Befehl ruft die Tresoreigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="04f0e-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="04f0e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04f0e-111">PARAMETERS</span></span>

### <span data-ttu-id="04f0e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f0e-112">-DefaultProfile</span></span>
<span data-ttu-id="04f0e-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04f0e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04f0e-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="04f0e-114">-VaultId</span></span>
<span data-ttu-id="04f0e-115">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="04f0e-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="04f0e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f0e-116">CommonParameters</span></span>
<span data-ttu-id="04f0e-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04f0e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f0e-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04f0e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f0e-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04f0e-119">INPUTS</span></span>

### <span data-ttu-id="04f0e-120">System.String</span><span class="sxs-lookup"><span data-stu-id="04f0e-120">System.String</span></span>

## <span data-ttu-id="04f0e-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04f0e-121">OUTPUTS</span></span>

### <span data-ttu-id="04f0e-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="04f0e-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="04f0e-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04f0e-123">NOTES</span></span>

## <span data-ttu-id="04f0e-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04f0e-124">RELATED LINKS</span></span>

[<span data-ttu-id="04f0e-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="04f0e-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="04f0e-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="04f0e-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
