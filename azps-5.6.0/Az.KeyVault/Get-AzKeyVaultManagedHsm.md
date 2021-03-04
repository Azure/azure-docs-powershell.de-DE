---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: b65fed5670f34072504c736283ba12e51086d3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941147"
---
# <span data-ttu-id="67b00-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="67b00-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="67b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67b00-102">SYNOPSIS</span></span>
<span data-ttu-id="67b00-103">Erhalten verwalteter HSMs.</span><span class="sxs-lookup"><span data-stu-id="67b00-103">Get managed HSMs.</span></span>

## <span data-ttu-id="67b00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67b00-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67b00-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67b00-105">DESCRIPTION</span></span>
<span data-ttu-id="67b00-106">Das **Get-AzKeyVaultManagedHsm-Cmdlet** ruft Informationen zu den verwalteten HSMs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="67b00-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="67b00-107">Sie können alle verwalteten HSMs-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten verwalteten HSM filtern.</span><span class="sxs-lookup"><span data-stu-id="67b00-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="67b00-108">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet zwar optional ist, wenn Sie ein einzelnes verwaltetes HSM erhalten, dies jedoch zur Besseren Leistung tun sollten.</span><span class="sxs-lookup"><span data-stu-id="67b00-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="67b00-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67b00-109">EXAMPLES</span></span>

### <span data-ttu-id="67b00-110">Beispiel 1: Alle verwalteten HSMs in Ihrem aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="67b00-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="67b00-111">Dieser Befehl ruft alle verwalteten HSMs in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="67b00-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="67b00-112">Beispiel 2: Erhalten eines bestimmten verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="67b00-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="67b00-113">Dieser Befehl ruft das verwaltete HSM mit dem Namen myhsm in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="67b00-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="67b00-114">Beispiel 3: Erhalten verwalteter HSMs in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="67b00-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="67b00-115">Dieser Befehl ruft alle verwalteten HSMs in der Ressourcengruppe myrg1 ab.</span><span class="sxs-lookup"><span data-stu-id="67b00-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="67b00-116">Beispiel 4: Erhalten verwalteter HSMs mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="67b00-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="67b00-117">Dieser Befehl ruft alle verwalteten HSMs im Abonnement ab, die mit "myhsm" beginnen.</span><span class="sxs-lookup"><span data-stu-id="67b00-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="67b00-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="67b00-118">PARAMETERS</span></span>

### <span data-ttu-id="67b00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b00-119">-DefaultProfile</span></span>
<span data-ttu-id="67b00-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67b00-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67b00-121">-Name</span><span class="sxs-lookup"><span data-stu-id="67b00-121">-Name</span></span>
<span data-ttu-id="67b00-122">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="67b00-122">HSM name.</span></span> <span data-ttu-id="67b00-123">Das Cmdlet erstellt den FQDN eines HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="67b00-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="67b00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b00-124">-ResourceGroupName</span></span>
<span data-ttu-id="67b00-125">Gibt den Namen der Ressourcengruppe an, die dem verwalteten HSM zugeordnet ist, das abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="67b00-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="67b00-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="67b00-126">-Tag</span></span>
<span data-ttu-id="67b00-127">Gibt den Schlüssel und optionalen Wert des angegebenen Tags an, nach dem die Liste der verwalteten HSMs gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="67b00-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b00-128">CommonParameters</span></span>
<span data-ttu-id="67b00-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b00-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67b00-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b00-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67b00-131">INPUTS</span></span>

### <span data-ttu-id="67b00-132">System.String</span><span class="sxs-lookup"><span data-stu-id="67b00-132">System.String</span></span>

### <span data-ttu-id="67b00-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="67b00-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="67b00-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67b00-134">OUTPUTS</span></span>

### <span data-ttu-id="67b00-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="67b00-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="67b00-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="67b00-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="67b00-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="67b00-137">NOTES</span></span>

## <span data-ttu-id="67b00-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="67b00-138">RELATED LINKS</span></span>

[<span data-ttu-id="67b00-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="67b00-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="67b00-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="67b00-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="67b00-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="67b00-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)