---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 72804d546869f2d003813c8e69c067ad23966fa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944075"
---
# <span data-ttu-id="0866f-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0866f-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="0866f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0866f-102">SYNOPSIS</span></span>
<span data-ttu-id="0866f-103">Erstellt ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="0866f-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="0866f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0866f-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0866f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0866f-105">DESCRIPTION</span></span>
<span data-ttu-id="0866f-106">Das **Cmdlet New-AzKeyVaultManagedHsm** erstellt ein verwaltetes HSM in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0866f-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="0866f-107">Zum Hinzufügen, Entfernen oder Auflisten von Schlüsseln im verwalteten HSM sollte der Benutzer Berechtigungen erteilen, indem er benutzer-ID zum Administrator hinzufügungen.</span><span class="sxs-lookup"><span data-stu-id="0866f-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="0866f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0866f-108">EXAMPLES</span></span>

### <span data-ttu-id="0866f-109">Beispiel 1: Erstellen eines von StandardB1 verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="0866f-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="0866f-110">Mit diesem Befehl wird ein verwaltetes HSM mit dem Namen myhsm an der Position eastus2euap erstellt.</span><span class="sxs-lookup"><span data-stu-id="0866f-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="0866f-111">Der Befehl fügt der Ressourcengruppe "myrg1" das verwaltete HSM hinzu.</span><span class="sxs-lookup"><span data-stu-id="0866f-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="0866f-112">Da mit dem Befehl kein Wert für den *SKU-Parameter* angegeben wird, wird ein Standard_B1 HSM erstellt.</span><span class="sxs-lookup"><span data-stu-id="0866f-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="0866f-113">Beispiel 2: Erstellen eines benutzerdefinierten B32-verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="0866f-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="0866f-114">Mit diesem Befehl wird ein verwaltetes HSM wie im vorherigen Beispiel erstellt.</span><span class="sxs-lookup"><span data-stu-id="0866f-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="0866f-115">Es gibt jedoch einen Wert von CustomB32 für den *SKU-Parameter* an, um ein benutzerdefiniertes B32-verwaltetes HSM zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0866f-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="0866f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0866f-116">PARAMETERS</span></span>

### <span data-ttu-id="0866f-117">-Administrator</span><span class="sxs-lookup"><span data-stu-id="0866f-117">-Administrator</span></span>
<span data-ttu-id="0866f-118">Erste Administratorobjekt-ID für diesen verwalteten HSM-Pool.</span><span class="sxs-lookup"><span data-stu-id="0866f-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0866f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0866f-119">-AsJob</span></span>
<span data-ttu-id="0866f-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0866f-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0866f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0866f-121">-DefaultProfile</span></span>
<span data-ttu-id="0866f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0866f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0866f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="0866f-123">-Location</span></span>
<span data-ttu-id="0866f-124">Gibt die Azure-Region an, in der der Schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0866f-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="0866f-125">Verwenden Sie den Befehl Get-AzResourceProvider mit dem Parameter ProviderNamespace, um Ihre Auswahlmöglichkeiten zu sehen.</span><span class="sxs-lookup"><span data-stu-id="0866f-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0866f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0866f-126">-Name</span></span>
<span data-ttu-id="0866f-127">Gibt einen Namen des verwalteten HSM an, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0866f-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="0866f-128">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="0866f-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="0866f-129">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="0866f-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="0866f-130">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0866f-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0866f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0866f-131">-ResourceGroupName</span></span>
<span data-ttu-id="0866f-132">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der Schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0866f-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0866f-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="0866f-133">-Sku</span></span>
<span data-ttu-id="0866f-134">Gibt die SKU der verwalteten HSM-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="0866f-134">Specifies the SKU of the managed HSM instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0866f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="0866f-135">-Tag</span></span>
<span data-ttu-id="0866f-136">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0866f-136">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0866f-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0866f-137">-Confirm</span></span>
<span data-ttu-id="0866f-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0866f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0866f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0866f-139">-WhatIf</span></span>
<span data-ttu-id="0866f-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0866f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0866f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0866f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0866f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0866f-142">CommonParameters</span></span>
<span data-ttu-id="0866f-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0866f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0866f-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0866f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0866f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0866f-145">INPUTS</span></span>

### <span data-ttu-id="0866f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="0866f-146">System.String</span></span>

### <span data-ttu-id="0866f-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0866f-147">System.String[]</span></span>

### <span data-ttu-id="0866f-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0866f-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0866f-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0866f-149">OUTPUTS</span></span>

### <span data-ttu-id="0866f-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0866f-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="0866f-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0866f-151">NOTES</span></span>

## <span data-ttu-id="0866f-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0866f-152">RELATED LINKS</span></span>

[<span data-ttu-id="0866f-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0866f-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="0866f-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0866f-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="0866f-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0866f-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)