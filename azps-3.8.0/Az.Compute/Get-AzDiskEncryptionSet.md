---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003645"
---
# <span data-ttu-id="59d96-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="59d96-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="59d96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59d96-102">SYNOPSIS</span></span>
<span data-ttu-id="59d96-103">Abrufen oder Auflisten von Datenträger Verschlüsselungs Sätzen</span><span class="sxs-lookup"><span data-stu-id="59d96-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="59d96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59d96-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59d96-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59d96-105">DESCRIPTION</span></span>
<span data-ttu-id="59d96-106">Abrufen oder Auflisten von Datenträger Verschlüsselungs Sätzen</span><span class="sxs-lookup"><span data-stu-id="59d96-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="59d96-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59d96-107">EXAMPLES</span></span>

### <span data-ttu-id="59d96-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59d96-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="59d96-109">Datenträger Verschlüsselungs Satz "ENC1" abrufen</span><span class="sxs-lookup"><span data-stu-id="59d96-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="59d96-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="59d96-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="59d96-111">Rufen Sie alle Datenträger Verschlüsselungs Sätze in der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="59d96-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="59d96-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="59d96-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="59d96-113">Alle Festplatten-Verschlüsselungs Sätze im Abonnement abrufen.</span><span class="sxs-lookup"><span data-stu-id="59d96-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="59d96-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="59d96-114">PARAMETERS</span></span>

### <span data-ttu-id="59d96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d96-115">-DefaultProfile</span></span>
<span data-ttu-id="59d96-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59d96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d96-117">-Name</span><span class="sxs-lookup"><span data-stu-id="59d96-117">-Name</span></span>
<span data-ttu-id="59d96-118">Name des Festplatten-Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="59d96-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d96-119">-ResourceGroupName</span></span>
<span data-ttu-id="59d96-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="59d96-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d96-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d96-121">CommonParameters</span></span>
<span data-ttu-id="59d96-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d96-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d96-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59d96-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d96-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59d96-124">INPUTS</span></span>

### <span data-ttu-id="59d96-125">System. String</span><span class="sxs-lookup"><span data-stu-id="59d96-125">System.String</span></span>

## <span data-ttu-id="59d96-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59d96-126">OUTPUTS</span></span>

### <span data-ttu-id="59d96-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="59d96-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="59d96-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="59d96-128">NOTES</span></span>

## <span data-ttu-id="59d96-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59d96-129">RELATED LINKS</span></span>
