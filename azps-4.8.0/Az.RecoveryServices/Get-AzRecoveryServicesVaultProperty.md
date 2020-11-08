---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165029"
---
# <span data-ttu-id="f59cf-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="f59cf-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="f59cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f59cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f59cf-103">Gibt die Eigenschaften eines Vault für Wiederherstellungsdienste zurück.</span><span class="sxs-lookup"><span data-stu-id="f59cf-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="f59cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f59cf-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f59cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f59cf-105">DESCRIPTION</span></span>
<span data-ttu-id="f59cf-106">Das Cmdlet " **Get-AzRecoveryServicesVaultProperty** " gibt die Eigenschaften eines Speichers für Wiederherstellungsdienste zurück.</span><span class="sxs-lookup"><span data-stu-id="f59cf-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="f59cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f59cf-107">EXAMPLES</span></span>

### <span data-ttu-id="f59cf-108">Beispiel 1: Abrufen von Eigenschaften eines Tresors</span><span class="sxs-lookup"><span data-stu-id="f59cf-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="f59cf-109">Der erste Befehl ruft ein Vault-Objekt ab und speichert es dann in der $Vault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f59cf-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="f59cf-110">Der zweite Befehl ruft die tresoreigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="f59cf-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="f59cf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f59cf-111">PARAMETERS</span></span>

### <span data-ttu-id="f59cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59cf-112">-DefaultProfile</span></span>
<span data-ttu-id="f59cf-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f59cf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f59cf-114">-Tresor</span><span class="sxs-lookup"><span data-stu-id="f59cf-114">-VaultId</span></span>
<span data-ttu-id="f59cf-115">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="f59cf-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f59cf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59cf-116">CommonParameters</span></span>
<span data-ttu-id="f59cf-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59cf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59cf-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f59cf-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59cf-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f59cf-119">INPUTS</span></span>

### <span data-ttu-id="f59cf-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f59cf-120">System.String</span></span>

## <span data-ttu-id="f59cf-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f59cf-121">OUTPUTS</span></span>

### <span data-ttu-id="f59cf-122">Microsoft. Azure. Management. RecoveryServices. Backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="f59cf-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="f59cf-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="f59cf-123">NOTES</span></span>

## <span data-ttu-id="f59cf-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f59cf-124">RELATED LINKS</span></span>

[<span data-ttu-id="f59cf-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f59cf-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f59cf-126">Satz-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="f59cf-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
