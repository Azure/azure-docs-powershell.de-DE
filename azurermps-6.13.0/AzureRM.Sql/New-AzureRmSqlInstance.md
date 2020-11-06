---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504286"
---
# <span data-ttu-id="42ca7-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42ca7-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="42ca7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="42ca7-103">Erstellt eine Azure SQL-Daten Bank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="42ca7-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42ca7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42ca7-104">SYNTAX</span></span>

### <span data-ttu-id="42ca7-105">NewByEditionAndComputeGenerationParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="42ca7-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ca7-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="42ca7-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ca7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42ca7-107">DESCRIPTION</span></span>
<span data-ttu-id="42ca7-108">Das Cmdlet **New-AzureRmSqlInstance** erstellt eine verwaltete Azure SQL-Datenbank-Instanz.</span><span class="sxs-lookup"><span data-stu-id="42ca7-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="42ca7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42ca7-109">EXAMPLES</span></span>

### <span data-ttu-id="42ca7-110">Beispiel 1: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="42ca7-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
```

<span data-ttu-id="42ca7-111">Mit diesem Befehl wird eine neue Instanz mithilfe von Edition-und ComputeGeneration-Parametern erstellt.</span><span class="sxs-lookup"><span data-stu-id="42ca7-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="42ca7-112">Beispiel 2: Erstellen einer neuen Instanz</span><span class="sxs-lookup"><span data-stu-id="42ca7-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
```

<span data-ttu-id="42ca7-113">Dieser Befehl erstellt eine neue Instanz mithilfe von Edition-und ComputeGeneration-Parametern.</span><span class="sxs-lookup"><span data-stu-id="42ca7-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="42ca7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="42ca7-114">PARAMETERS</span></span>

### <span data-ttu-id="42ca7-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="42ca7-115">-AdministratorCredential</span></span>
<span data-ttu-id="42ca7-116">Die SQL-Authentifizierungsanmeldeinformationen der Instanz.</span><span class="sxs-lookup"><span data-stu-id="42ca7-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42ca7-117">-AsJob</span></span>
<span data-ttu-id="42ca7-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="42ca7-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="42ca7-119">-AssignIdentity</span></span>
<span data-ttu-id="42ca7-120">Generieren Sie eine Azure Active Directory-Identität für diese verwaltete Instanz, und weisen Sie Sie für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault zu.</span><span class="sxs-lookup"><span data-stu-id="42ca7-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-121">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="42ca7-121">-ComputeGeneration</span></span>
<span data-ttu-id="42ca7-122">Die COMPUTE-Generierung für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="42ca7-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ca7-123">-DefaultProfile</span></span>
<span data-ttu-id="42ca7-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42ca7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="42ca7-125">-Edition</span></span>
<span data-ttu-id="42ca7-126">Die Edition für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="42ca7-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="42ca7-127">-LicenseType</span></span>
<span data-ttu-id="42ca7-128">Ermitteln des zu verwendenden Lizenztyps der Instanz</span><span class="sxs-lookup"><span data-stu-id="42ca7-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="42ca7-129">-Location</span></span>
<span data-ttu-id="42ca7-130">Die Position, an der die Instanz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="42ca7-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-131">-Name</span><span class="sxs-lookup"><span data-stu-id="42ca7-131">-Name</span></span>
<span data-ttu-id="42ca7-132">Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="42ca7-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42ca7-133">-ResourceGroupName</span></span>
<span data-ttu-id="42ca7-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42ca7-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-135">-SkuName</span><span class="sxs-lookup"><span data-stu-id="42ca7-135">-SkuName</span></span>
<span data-ttu-id="42ca7-136">Der SKU-Name für die Instanz, beispielsweise "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="42ca7-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="42ca7-137">-StorageSizeInGB</span></span>
<span data-ttu-id="42ca7-138">Bestimmt, wie viel Speichergröße mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="42ca7-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-139">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="42ca7-139">-SubnetId</span></span>
<span data-ttu-id="42ca7-140">Die für die Erstellung von Instanzen zu verwendende Subnetz-ID</span><span class="sxs-lookup"><span data-stu-id="42ca7-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="42ca7-141">-Tag</span></span>
<span data-ttu-id="42ca7-142">Die Tags, die der Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42ca7-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="42ca7-143">-VCore</span></span>
<span data-ttu-id="42ca7-144">Bestimmt, wie viel Vcore mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="42ca7-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42ca7-145">-Confirm</span></span>
<span data-ttu-id="42ca7-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42ca7-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ca7-147">-WhatIf</span></span>
<span data-ttu-id="42ca7-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42ca7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42ca7-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42ca7-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ca7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ca7-150">CommonParameters</span></span>
<span data-ttu-id="42ca7-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ca7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ca7-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ca7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ca7-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42ca7-153">INPUTS</span></span>

### <span data-ttu-id="42ca7-154">Keine</span><span class="sxs-lookup"><span data-stu-id="42ca7-154">None</span></span>

## <span data-ttu-id="42ca7-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42ca7-155">OUTPUTS</span></span>

### <span data-ttu-id="42ca7-156">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="42ca7-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="42ca7-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="42ca7-157">NOTES</span></span>

## <span data-ttu-id="42ca7-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42ca7-158">RELATED LINKS</span></span>
