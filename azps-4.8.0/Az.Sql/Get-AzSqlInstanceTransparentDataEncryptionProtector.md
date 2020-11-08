---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174127"
---
# <span data-ttu-id="d1348-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d1348-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="d1348-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1348-102">SYNOPSIS</span></span>
<span data-ttu-id="d1348-103">Ruft die transparente Daten Verschlüsselungs-Beschützer für eine verwaltete SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="d1348-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="d1348-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1348-104">SYNTAX</span></span>

### <span data-ttu-id="d1348-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1348-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1348-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1348-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1348-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1348-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1348-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1348-108">DESCRIPTION</span></span>
<span data-ttu-id="d1348-109">Das Get-AzSqlInstanceTransparentDataEncryptionProtector-Cmdlet ruft die DSA-Beschützer für die angegebene verwaltete SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="d1348-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="d1348-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1348-110">EXAMPLES</span></span>

### <span data-ttu-id="d1348-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1348-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="d1348-112">Dieser Befehl ruft die DSA-Beschützer für die verwaltete Instanz mit dem Namen ContosoManagedInstanceName in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d1348-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="d1348-113">Beispiel 2: Verwenden eines verwalteten Instanzen Objekts</span><span class="sxs-lookup"><span data-stu-id="d1348-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="d1348-114">Dieser Befehl ruft die DSA-Beschützer für die verwaltete Instanz mit dem Namen ContosoManagedInstanceName in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d1348-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="d1348-115">Beispiel 3: Verwenden der Ressourcen-ID für verwaltete Instanzen</span><span class="sxs-lookup"><span data-stu-id="d1348-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="d1348-116">Dieser Befehl ruft die DSA-Beschützer für die verwaltete Instanz mit dem Namen ContosoManagedInstanceName in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d1348-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="d1348-117">Beispiel 4: Verwenden von Piping</span><span class="sxs-lookup"><span data-stu-id="d1348-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="d1348-118">Dieser Befehl ruft die DSA-Beschützer für die verwaltete Instanz mit dem Namen ContosoManagedInstanceName in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d1348-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="d1348-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1348-119">PARAMETERS</span></span>

### <span data-ttu-id="d1348-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1348-120">-DefaultProfile</span></span>
<span data-ttu-id="d1348-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1348-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1348-122">-Instanz</span><span class="sxs-lookup"><span data-stu-id="d1348-122">-Instance</span></span>
<span data-ttu-id="d1348-123">Das Instanzen Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="d1348-123">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1348-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d1348-124">-InstanceName</span></span>
<span data-ttu-id="d1348-125">Der Instanzname</span><span class="sxs-lookup"><span data-stu-id="d1348-125">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1348-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d1348-126">-InstanceResourceId</span></span>
<span data-ttu-id="d1348-127">Die Ressourcen-ID der Instanz</span><span class="sxs-lookup"><span data-stu-id="d1348-127">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1348-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1348-128">-ResourceGroupName</span></span>
<span data-ttu-id="d1348-129">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d1348-129">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1348-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1348-130">-Confirm</span></span>
<span data-ttu-id="d1348-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1348-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1348-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1348-132">-WhatIf</span></span>
<span data-ttu-id="d1348-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1348-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1348-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1348-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1348-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1348-135">CommonParameters</span></span>
<span data-ttu-id="d1348-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1348-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1348-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1348-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1348-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1348-138">INPUTS</span></span>

### <span data-ttu-id="d1348-139">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d1348-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="d1348-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d1348-140">System.String</span></span>

## <span data-ttu-id="d1348-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1348-141">OUTPUTS</span></span>

### <span data-ttu-id="d1348-142">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="d1348-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="d1348-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1348-143">NOTES</span></span>

## <span data-ttu-id="d1348-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1348-144">RELATED LINKS</span></span>
