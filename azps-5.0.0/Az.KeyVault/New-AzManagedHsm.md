---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180416"
---
# <span data-ttu-id="b2310-101">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b2310-101">New-AzManagedHsm</span></span>

## <span data-ttu-id="b2310-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2310-102">SYNOPSIS</span></span>
<span data-ttu-id="b2310-103">Erstellt ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="b2310-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="b2310-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2310-104">SYNTAX</span></span>

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2310-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2310-105">DESCRIPTION</span></span>
<span data-ttu-id="b2310-106">Mit dem Cmdlet **New-AzManagedHsm** wird ein verwaltetes HSM in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2310-106">The **New-AzManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="b2310-107">Zum Hinzufügen, entfernen oder Auflisten von Schlüsseln im verwalteten HSM sollte der Benutzerberechtigungen erteilen, indem er dem Administrator eine Benutzer-ID hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b2310-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="b2310-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2310-108">EXAMPLES</span></span>

### <span data-ttu-id="b2310-109">Beispiel 1: Erstellen eines StandardB1-verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="b2310-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="b2310-110">Mit diesem Befehl wird ein verwaltetes HSM mit dem Namen myhsm am Standort eastus2euap erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2310-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="b2310-111">Der Befehl fügt das verwaltete HSM zur Ressourcengruppe mit dem Namen myrg1 hinzu.</span><span class="sxs-lookup"><span data-stu-id="b2310-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="b2310-112">Da der Befehl keinen Wert für den *SKU* -Parameter angibt, wird ein Standard_B1 verwaltetes HSM erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2310-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="b2310-113">Beispiel 2: Erstellen eines CustomB32-verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="b2310-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="b2310-114">Mit diesem Befehl wird ein verwaltetes HSM erstellt, genau wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="b2310-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="b2310-115">Es gibt jedoch einen Wert von CustomB32 für den *SKU* -Parameter an, um ein CustomB32 verwaltetes HSM zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2310-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="b2310-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2310-116">PARAMETERS</span></span>

### <span data-ttu-id="b2310-117">– Administrator</span><span class="sxs-lookup"><span data-stu-id="b2310-117">-Administrator</span></span>
<span data-ttu-id="b2310-118">Anfängliche Administrator Objekt-ID für diesen verwalteten HSM-Pool.</span><span class="sxs-lookup"><span data-stu-id="b2310-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="b2310-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2310-119">-AsJob</span></span>
<span data-ttu-id="b2310-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b2310-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2310-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2310-121">-DefaultProfile</span></span>
<span data-ttu-id="b2310-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2310-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2310-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="b2310-123">-Location</span></span>
<span data-ttu-id="b2310-124">Gibt den Azure-Bereich an, in dem der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2310-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="b2310-125">Verwenden Sie den Befehl Get-AzResourceProvider mit dem ProviderNamespace-Parameter, um Ihre Auswahlmöglichkeiten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2310-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="b2310-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b2310-126">-Name</span></span>
<span data-ttu-id="b2310-127">Gibt den Namen des verwalteten HSM an, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2310-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="b2310-128">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="b2310-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="b2310-129">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="b2310-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="b2310-130">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="b2310-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="b2310-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2310-131">-ResourceGroupName</span></span>
<span data-ttu-id="b2310-132">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2310-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="b2310-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="b2310-133">-Sku</span></span>
<span data-ttu-id="b2310-134">Gibt die SKU der verwalteten HSM-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="b2310-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="b2310-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2310-135">-Tag</span></span>
<span data-ttu-id="b2310-136">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2310-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b2310-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2310-137">-Confirm</span></span>
<span data-ttu-id="b2310-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2310-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2310-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2310-139">-WhatIf</span></span>
<span data-ttu-id="b2310-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2310-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2310-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2310-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2310-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2310-142">CommonParameters</span></span>
<span data-ttu-id="b2310-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2310-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2310-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2310-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2310-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2310-145">INPUTS</span></span>

### <span data-ttu-id="b2310-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b2310-146">System.String</span></span>

### <span data-ttu-id="b2310-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="b2310-147">System.String[]</span></span>

### <span data-ttu-id="b2310-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2310-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b2310-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2310-149">OUTPUTS</span></span>

### <span data-ttu-id="b2310-150">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b2310-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="b2310-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2310-151">NOTES</span></span>

## <span data-ttu-id="b2310-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2310-152">RELATED LINKS</span></span>

[<span data-ttu-id="b2310-153">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b2310-153">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="b2310-154">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b2310-154">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="b2310-155">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b2310-155">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)