---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004921"
---
# <span data-ttu-id="b7f01-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="b7f01-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="b7f01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7f01-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f01-103">Gibt die Eigenschaften eines Vault für Wiederherstellungsdienste zurück.</span><span class="sxs-lookup"><span data-stu-id="b7f01-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="b7f01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7f01-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7f01-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7f01-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f01-106">Das Cmdlet " **Get-AzRecoveryServicesVaultProperty** " gibt die Eigenschaften eines Speichers für Wiederherstellungsdienste zurück.</span><span class="sxs-lookup"><span data-stu-id="b7f01-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="b7f01-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7f01-107">EXAMPLES</span></span>

### <span data-ttu-id="b7f01-108">Beispiel 1: Abrufen von Eigenschaften eines Tresors</span><span class="sxs-lookup"><span data-stu-id="b7f01-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="b7f01-109">Der erste Befehl ruft ein Vault-Objekt ab und speichert es dann in der $Vault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b7f01-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="b7f01-110">Der zweite Befehl ruft die tresoreigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="b7f01-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="b7f01-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7f01-111">PARAMETERS</span></span>

### <span data-ttu-id="b7f01-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f01-112">-DefaultProfile</span></span>
<span data-ttu-id="b7f01-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7f01-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7f01-114">-Tresor</span><span class="sxs-lookup"><span data-stu-id="b7f01-114">-VaultId</span></span>
<span data-ttu-id="b7f01-115">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="b7f01-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b7f01-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f01-116">CommonParameters</span></span>
<span data-ttu-id="b7f01-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f01-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f01-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7f01-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f01-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7f01-119">INPUTS</span></span>

### <span data-ttu-id="b7f01-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b7f01-120">System.String</span></span>

## <span data-ttu-id="b7f01-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7f01-121">OUTPUTS</span></span>

### <span data-ttu-id="b7f01-122">Microsoft. Azure. Management. RecoveryServices. Backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="b7f01-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="b7f01-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7f01-123">NOTES</span></span>

## <span data-ttu-id="b7f01-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7f01-124">RELATED LINKS</span></span>

[<span data-ttu-id="b7f01-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b7f01-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="b7f01-126">Satz-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="b7f01-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
