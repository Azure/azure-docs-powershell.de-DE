---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
ms.openlocfilehash: 1e992e33591f5c993bfdda1bf9934245b2f5f2c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501950"
---
# <span data-ttu-id="0f8c4-101">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0f8c4-101">Set-AzureRmSqlInstance</span></span>

## <span data-ttu-id="0f8c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8c4-103">Legt Eigenschaften für eine Azure SQL-Daten Bank verwaltete Instanz fest.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f8c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f8c4-104">SYNTAX</span></span>

### <span data-ttu-id="0f8c4-105">SetInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f8c4-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f8c4-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="0f8c4-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f8c4-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="0f8c4-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzureRmSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>] [-AssignIdentity]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f8c4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f8c4-108">DESCRIPTION</span></span>
<span data-ttu-id="0f8c4-109">Das Cmdlet " **Satz-AzureRmSqlInstance** " ändert die Eigenschaften einer Azure SQL-Datenbank-verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-109">The **Set-AzureRmSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="0f8c4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f8c4-110">EXAMPLES</span></span>

### <span data-ttu-id="0f8c4-111">Beispiel 1: Setzen einer vorhandenen Instanz mit neuen Werten für-Administrator Password,-LicenseType,-StorageSizeInGB und-VCore</span><span class="sxs-lookup"><span data-stu-id="0f8c4-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="0f8c4-112">Dieser Befehl legt die vorhandene Instanz mit neuen Werten für-Administrator Password,-LicenseType,-StorageSizeInGB und-Vcore fest.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="0f8c4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f8c4-113">PARAMETERS</span></span>

### <span data-ttu-id="0f8c4-114">-Administrator Password</span><span class="sxs-lookup"><span data-stu-id="0f8c4-114">-AdministratorPassword</span></span>
<span data-ttu-id="0f8c4-115">Das neue SQL-Administratorkennwort für die Instanz.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-115">The new SQL administrator password for the instance.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0f8c4-116">-AssignIdentity</span></span>
<span data-ttu-id="0f8c4-117">Generieren Sie eine Azure Active Directory-Identität für diese Instanz, und weisen Sie Sie für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault zu.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0f8c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8c4-118">-DefaultProfile</span></span>
<span data-ttu-id="0f8c4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f8c4-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="0f8c4-120">-Edition</span></span>
<span data-ttu-id="0f8c4-121">Die Edition, die der Instanz zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-121">The edition to assign to the instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0f8c4-122">-Force</span></span>
<span data-ttu-id="0f8c4-123">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="0f8c4-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0f8c4-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0f8c4-124">-InputObject</span></span>
<span data-ttu-id="0f8c4-125">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="0f8c4-125">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0f8c4-126">-LicenseType</span></span>
<span data-ttu-id="0f8c4-127">Ermitteln des zu verwendenden Lizenztyps der Instanz</span><span class="sxs-lookup"><span data-stu-id="0f8c4-127">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0f8c4-128">-Name</span></span>
<span data-ttu-id="0f8c4-129">Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-129">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f8c4-130">-ResourceGroupName</span></span>
<span data-ttu-id="0f8c4-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0f8c4-132">-ResourceId</span></span>
<span data-ttu-id="0f8c4-133">Die Ressourcen-ID der zu entfernenden Instanz</span><span class="sxs-lookup"><span data-stu-id="0f8c4-133">The resource id of instance to remove</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-134">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0f8c4-134">-StorageSizeInGB</span></span>
<span data-ttu-id="0f8c4-135">Bestimmt, wie viel Speichergröße mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-135">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f8c4-136">-Tag</span></span>
<span data-ttu-id="0f8c4-137">Die Tags, die der Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-137">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="0f8c4-138">-VCore</span><span class="sxs-lookup"><span data-stu-id="0f8c4-138">-VCore</span></span>
<span data-ttu-id="0f8c4-139">Bestimmt, wie viel Vcore mit der Instanz verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-139">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c4-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0f8c4-140">-Confirm</span></span>
<span data-ttu-id="0f8c4-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f8c4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f8c4-142">-WhatIf</span></span>
<span data-ttu-id="0f8c4-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f8c4-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f8c4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8c4-145">CommonParameters</span></span>
<span data-ttu-id="0f8c4-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f8c4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8c4-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8c4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8c4-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f8c4-148">INPUTS</span></span>

### <span data-ttu-id="0f8c4-149">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="0f8c4-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="0f8c4-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0f8c4-150">System.String</span></span>

## <span data-ttu-id="0f8c4-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f8c4-151">OUTPUTS</span></span>

### <span data-ttu-id="0f8c4-152">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="0f8c4-152">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="0f8c4-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f8c4-153">NOTES</span></span>

## <span data-ttu-id="0f8c4-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f8c4-154">RELATED LINKS</span></span>
