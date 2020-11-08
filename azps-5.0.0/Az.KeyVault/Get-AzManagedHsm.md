---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177933"
---
# <span data-ttu-id="0c298-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0c298-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="0c298-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c298-102">SYNOPSIS</span></span>
<span data-ttu-id="0c298-103">Abrufen verwalteter HSMs.</span><span class="sxs-lookup"><span data-stu-id="0c298-103">Get managed HSMs.</span></span>

## <span data-ttu-id="0c298-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c298-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c298-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c298-105">DESCRIPTION</span></span>
<span data-ttu-id="0c298-106">Das Cmdlet " **Get-AzManagedHsm** " Ruft Informationen zur verwalteten HSMs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0c298-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="0c298-107">Sie können alle verwalteten HSMs-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten verwalteten HSM filtern.</span><span class="sxs-lookup"><span data-stu-id="0c298-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="0c298-108">Beachten Sie, dass die Angabe der Ressourcengruppe zwar für dieses Cmdlet optional ist, wenn Sie ein einzelnes verwaltetes HSM erhalten, Sie dies jedoch für eine bessere Leistung tun sollten.</span><span class="sxs-lookup"><span data-stu-id="0c298-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="0c298-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c298-109">EXAMPLES</span></span>

### <span data-ttu-id="0c298-110">Beispiel 1: Abrufen aller verwalteten HSMs in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="0c298-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="0c298-111">Dieser Befehl ruft alle verwalteten HSMs in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0c298-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="0c298-112">Beispiel 2: Abrufen eines bestimmten verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="0c298-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="0c298-113">Dieser Befehl ruft das verwaltete HSM mit dem Namen myhsm in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0c298-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="0c298-114">Beispiel 3: Abrufen von verwalteten HSMs in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0c298-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="0c298-115">Dieser Befehl ruft alle verwalteten HSMs in der Ressourcengruppe mit dem Namen myrg1 ab.</span><span class="sxs-lookup"><span data-stu-id="0c298-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="0c298-116">Beispiel 4: Abrufen verwalteter HSMs mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="0c298-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="0c298-117">Dieser Befehl ruft alle verwalteten HSMs im Abonnement ab, die mit "myhsm" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0c298-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="0c298-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c298-118">PARAMETERS</span></span>

### <span data-ttu-id="0c298-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c298-119">-DefaultProfile</span></span>
<span data-ttu-id="0c298-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c298-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c298-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0c298-121">-Name</span></span>
<span data-ttu-id="0c298-122">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="0c298-122">HSM name.</span></span> <span data-ttu-id="0c298-123">Cmdlet erstellt den FQDN eines HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0c298-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c298-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c298-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c298-125">Gibt den Namen der Ressourcengruppe an, die dem verwalteten HSM zugeordnet ist, das abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="0c298-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c298-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c298-126">-Tag</span></span>
<span data-ttu-id="0c298-127">Gibt den Schlüssel und optionalen Wert des angegebenen Tags an, um die Liste der verwalteten HSMs zu filtern.</span><span class="sxs-lookup"><span data-stu-id="0c298-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="0c298-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c298-128">CommonParameters</span></span>
<span data-ttu-id="0c298-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c298-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c298-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c298-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c298-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c298-131">INPUTS</span></span>

### <span data-ttu-id="0c298-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0c298-132">System.String</span></span>

### <span data-ttu-id="0c298-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0c298-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0c298-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c298-134">OUTPUTS</span></span>

### <span data-ttu-id="0c298-135">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0c298-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="0c298-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0c298-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="0c298-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c298-137">NOTES</span></span>

## <span data-ttu-id="0c298-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c298-138">RELATED LINKS</span></span>

[<span data-ttu-id="0c298-139">Neu – AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0c298-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="0c298-140">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0c298-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="0c298-141">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0c298-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)