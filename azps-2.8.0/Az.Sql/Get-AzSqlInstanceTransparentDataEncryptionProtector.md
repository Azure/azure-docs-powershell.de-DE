---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 827c3c3d3cb87fbc3e51b8f083c74af559152115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825539"
---
# <span data-ttu-id="5a373-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5a373-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="5a373-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a373-102">SYNOPSIS</span></span>
<span data-ttu-id="5a373-103">Ruft die transparente Daten Verschlüsselungs-Beschützer für eine verwaltete SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="5a373-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="5a373-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a373-104">SYNTAX</span></span>

### <span data-ttu-id="5a373-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a373-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a373-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a373-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a373-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a373-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a373-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a373-108">DESCRIPTION</span></span>
<span data-ttu-id="5a373-109">Das Get-AzSqlInstanceTransparentDataEncryptionProtector-Cmdlet ruft die DSA-Beschützer für die angegebene verwaltete SQL-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="5a373-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="5a373-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a373-110">EXAMPLES</span></span>

### <span data-ttu-id="5a373-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a373-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="5a373-112">Dieser Befehl ruft die DSA-Beschützer für die verwaltete Instanz mit dem Namen ContosoManagedInstanceName in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5a373-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="5a373-113">Beispiel 2: Verwenden eines verwalteten Instanzen Objekts</span><span class="sxs-lookup"><span data-stu-id="5a373-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="5a373-114">Dieser Befehl ruft die DSA-Beschützer für die verwaltete Instanz mit dem Namen ContosoManagedInstanceName in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5a373-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="5a373-115">Beispiel 3: Verwenden der Ressourcen-ID für verwaltete Instanzen</span><span class="sxs-lookup"><span data-stu-id="5a373-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="5a373-116">Dieser Befehl ruft die DSA-Beschützer für die verwaltete Instanz mit dem Namen ContosoManagedInstanceName in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5a373-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="5a373-117">Beispiel 4: Verwenden von Piping</span><span class="sxs-lookup"><span data-stu-id="5a373-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="5a373-118">Dieser Befehl ruft die DSA-Beschützer für die verwaltete Instanz mit dem Namen ContosoManagedInstanceName in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5a373-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="5a373-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a373-119">PARAMETERS</span></span>

### <span data-ttu-id="5a373-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a373-120">-DefaultProfile</span></span>
<span data-ttu-id="5a373-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a373-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a373-122">-Instanz</span><span class="sxs-lookup"><span data-stu-id="5a373-122">-Instance</span></span>
<span data-ttu-id="5a373-123">Das Instanzen Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5a373-123">The instance input object</span></span>

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

### <span data-ttu-id="5a373-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5a373-124">-InstanceName</span></span>
<span data-ttu-id="5a373-125">Der Instanzname</span><span class="sxs-lookup"><span data-stu-id="5a373-125">The instance name</span></span>

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

### <span data-ttu-id="5a373-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="5a373-126">-InstanceResourceId</span></span>
<span data-ttu-id="5a373-127">Die Ressourcen-ID der Instanz</span><span class="sxs-lookup"><span data-stu-id="5a373-127">The instance resource id</span></span>

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

### <span data-ttu-id="5a373-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a373-128">-ResourceGroupName</span></span>
<span data-ttu-id="5a373-129">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5a373-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="5a373-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a373-130">-Confirm</span></span>
<span data-ttu-id="5a373-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a373-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a373-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a373-132">-WhatIf</span></span>
<span data-ttu-id="5a373-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a373-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a373-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a373-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a373-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a373-135">CommonParameters</span></span>
<span data-ttu-id="5a373-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a373-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a373-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a373-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a373-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a373-138">INPUTS</span></span>

### <span data-ttu-id="5a373-139">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="5a373-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="5a373-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5a373-140">System.String</span></span>

## <span data-ttu-id="5a373-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a373-141">OUTPUTS</span></span>

### <span data-ttu-id="5a373-142">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="5a373-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="5a373-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a373-143">NOTES</span></span>

## <span data-ttu-id="5a373-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a373-144">RELATED LINKS</span></span>
