---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296260"
---
# <span data-ttu-id="b1277-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b1277-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="b1277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1277-102">SYNOPSIS</span></span>
<span data-ttu-id="b1277-103">Erstellt einen verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="b1277-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="b1277-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1277-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1277-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1277-105">DESCRIPTION</span></span>
<span data-ttu-id="b1277-106">Das **Cmdlet "New-AzKeyVaultManagedHsm"** erstellt ein verwaltetes HSM in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b1277-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="b1277-107">Zum Hinzufügen, Entfernen oder Auflisten von Schlüsseln im verwalteten HSM sollte der Benutzer Berechtigungen erteilen, indem er die Benutzer-ID dem Administrator hinzu fügt.</span><span class="sxs-lookup"><span data-stu-id="b1277-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="b1277-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1277-108">EXAMPLES</span></span>

### <span data-ttu-id="b1277-109">Beispiel 1: Erstellen eines verwalteten HSM mit StandardB1</span><span class="sxs-lookup"><span data-stu-id="b1277-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="b1277-110">Dieser Befehl erstellt einen verwalteten HSM mit dem Namen "myhsm" am Speicherort "eastus2euap".</span><span class="sxs-lookup"><span data-stu-id="b1277-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="b1277-111">Der Befehl fügt den verwalteten HSM der Ressourcengruppe "myrg1" hinzu.</span><span class="sxs-lookup"><span data-stu-id="b1277-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="b1277-112">Da der Befehl keinen Wert für den *SKU-Parameter* anfordert, wird Standard_B1 HSM erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1277-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="b1277-113">Beispiel 2: Erstellen eines benutzerdefiniertenB32-verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="b1277-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="b1277-114">Mit diesem Befehl wird wie im vorherigen Beispiel ein verwalteter HSM erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1277-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="b1277-115">Es gibt jedoch den Wert "CustomB32" für den Parameter *"SKU"* an, um einen benutzerdefiniertenB32-verwalteten HSM zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1277-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="b1277-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1277-116">PARAMETERS</span></span>

### <span data-ttu-id="b1277-117">-Administrator</span><span class="sxs-lookup"><span data-stu-id="b1277-117">-Administrator</span></span>
<span data-ttu-id="b1277-118">Die anfängliche Administratorobjekt-ID für diesen verwalteten HSM-Pool.</span><span class="sxs-lookup"><span data-stu-id="b1277-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="b1277-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1277-119">-AsJob</span></span>
<span data-ttu-id="b1277-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b1277-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1277-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1277-121">-DefaultProfile</span></span>
<span data-ttu-id="b1277-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1277-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1277-123">-Location</span><span class="sxs-lookup"><span data-stu-id="b1277-123">-Location</span></span>
<span data-ttu-id="b1277-124">Gibt die Azure-Region an, in der der Schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1277-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="b1277-125">Verwenden Sie den Befehl Get-AzResourceProvider mit dem Parameter "ProviderNamespace", um Ihre Auswahlmöglichkeiten zu sehen.</span><span class="sxs-lookup"><span data-stu-id="b1277-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="b1277-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b1277-126">-Name</span></span>
<span data-ttu-id="b1277-127">Gibt einen Namen des verwalteten HSM an, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1277-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="b1277-128">Bei dem Namen kann es sich um eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen geben.</span><span class="sxs-lookup"><span data-stu-id="b1277-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="b1277-129">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="b1277-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="b1277-130">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="b1277-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="b1277-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1277-131">-ResourceGroupName</span></span>
<span data-ttu-id="b1277-132">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der Schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1277-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="b1277-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="b1277-133">-Sku</span></span>
<span data-ttu-id="b1277-134">Gibt die SKU der verwalteten HSM-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="b1277-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="b1277-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1277-135">-Tag</span></span>
<span data-ttu-id="b1277-136">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1277-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b1277-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1277-137">-Confirm</span></span>
<span data-ttu-id="b1277-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1277-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1277-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b1277-139">-WhatIf</span></span>
<span data-ttu-id="b1277-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1277-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1277-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1277-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1277-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1277-142">CommonParameters</span></span>
<span data-ttu-id="b1277-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1277-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1277-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1277-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1277-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1277-145">INPUTS</span></span>

### <span data-ttu-id="b1277-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b1277-146">System.String</span></span>

### <span data-ttu-id="b1277-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b1277-147">System.String[]</span></span>

### <span data-ttu-id="b1277-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b1277-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b1277-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1277-149">OUTPUTS</span></span>

### <span data-ttu-id="b1277-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b1277-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="b1277-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b1277-151">NOTES</span></span>

## <span data-ttu-id="b1277-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b1277-152">RELATED LINKS</span></span>

[<span data-ttu-id="b1277-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b1277-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="b1277-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b1277-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="b1277-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b1277-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)