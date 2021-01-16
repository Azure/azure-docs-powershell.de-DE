---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294149"
---
# <span data-ttu-id="4fd19-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4fd19-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="4fd19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd19-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd19-103">Sätze für die Datenträgerverschlüsselung erhalten oder auflisten</span><span class="sxs-lookup"><span data-stu-id="4fd19-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="4fd19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fd19-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd19-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fd19-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd19-106">Sätze für die Datenträgerverschlüsselung erhalten oder auflisten</span><span class="sxs-lookup"><span data-stu-id="4fd19-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="4fd19-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4fd19-107">EXAMPLES</span></span>

### <span data-ttu-id="4fd19-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4fd19-108">Example 1</span></span>
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

<span data-ttu-id="4fd19-109">Laufwerkverschlüsselungssatz 'enc1' erhalten</span><span class="sxs-lookup"><span data-stu-id="4fd19-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="4fd19-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4fd19-110">Example 2</span></span>
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

<span data-ttu-id="4fd19-111">Alle Datenträgerverschlüsselungssätze in der Ressourcengruppe "rg1" erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fd19-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="4fd19-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4fd19-112">Example 3</span></span>
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

<span data-ttu-id="4fd19-113">Holen Sie sich alle Datenträgerverschlüsselungssätze im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4fd19-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="4fd19-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fd19-114">PARAMETERS</span></span>

### <span data-ttu-id="4fd19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd19-115">-DefaultProfile</span></span>
<span data-ttu-id="4fd19-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fd19-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd19-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4fd19-117">-Name</span></span>
<span data-ttu-id="4fd19-118">Name des Datenträgerverschlüsselungssatzs.</span><span class="sxs-lookup"><span data-stu-id="4fd19-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="4fd19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd19-119">-ResourceGroupName</span></span>
<span data-ttu-id="4fd19-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4fd19-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4fd19-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd19-121">CommonParameters</span></span>
<span data-ttu-id="4fd19-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd19-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd19-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fd19-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd19-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4fd19-124">INPUTS</span></span>

### <span data-ttu-id="4fd19-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4fd19-125">System.String</span></span>

## <span data-ttu-id="4fd19-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4fd19-126">OUTPUTS</span></span>

### <span data-ttu-id="4fd19-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4fd19-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="4fd19-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4fd19-128">NOTES</span></span>

## <span data-ttu-id="4fd19-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4fd19-129">RELATED LINKS</span></span>
