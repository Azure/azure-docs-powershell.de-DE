---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 98538ba503b1fa31ae4c14897d56b0e0b9daffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943325"
---
# <span data-ttu-id="c56e6-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c56e6-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="c56e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c56e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c56e6-103">Ruft den Schutz für transparente Datenverschlüsselung (Transparent Data Encryption, TDE) für eine verwaltete SQL ab.</span><span class="sxs-lookup"><span data-stu-id="c56e6-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="c56e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c56e6-104">SYNTAX</span></span>

### <span data-ttu-id="c56e6-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c56e6-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c56e6-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c56e6-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c56e6-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c56e6-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56e6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c56e6-108">DESCRIPTION</span></span>
<span data-ttu-id="c56e6-109">Das Get-AzSqlInstanceTransparentDataEncryptionProtector-Cmdlet ruft den TDE-Protektor für die angegebene verwaltete SQL ab.</span><span class="sxs-lookup"><span data-stu-id="c56e6-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="c56e6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c56e6-110">EXAMPLES</span></span>

### <span data-ttu-id="c56e6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c56e6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c56e6-112">Dieser Befehl ruft den TDE-Protektor für die verwaltete Instanz namens ContosoManagedInstanceName in der Ressourcengruppe ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c56e6-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c56e6-113">Beispiel 2: Verwenden eines verwalteten Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="c56e6-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c56e6-114">Dieser Befehl ruft den TDE-Protektor für die verwaltete Instanz namens ContosoManagedInstanceName in der Ressourcengruppe ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c56e6-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c56e6-115">Beispiel 3: Verwenden der Ressourcen-ID für verwaltete Instanzen</span><span class="sxs-lookup"><span data-stu-id="c56e6-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c56e6-116">Dieser Befehl ruft den TDE-Protektor für die verwaltete Instanz namens ContosoManagedInstanceName in der Ressourcengruppe ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c56e6-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c56e6-117">Beispiel 4: Verwenden von Piping</span><span class="sxs-lookup"><span data-stu-id="c56e6-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c56e6-118">Dieser Befehl ruft den TDE-Protektor für die verwaltete Instanz namens ContosoManagedInstanceName in der Ressourcengruppe ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c56e6-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c56e6-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c56e6-119">PARAMETERS</span></span>

### <span data-ttu-id="c56e6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56e6-120">-DefaultProfile</span></span>
<span data-ttu-id="c56e6-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c56e6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c56e6-122">-Instanz</span><span class="sxs-lookup"><span data-stu-id="c56e6-122">-Instance</span></span>
<span data-ttu-id="c56e6-123">Das Instanzeingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="c56e6-123">The instance input object</span></span>

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

### <span data-ttu-id="c56e6-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c56e6-124">-InstanceName</span></span>
<span data-ttu-id="c56e6-125">Der Name der Instanz</span><span class="sxs-lookup"><span data-stu-id="c56e6-125">The instance name</span></span>

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

### <span data-ttu-id="c56e6-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="c56e6-126">-InstanceResourceId</span></span>
<span data-ttu-id="c56e6-127">Die Instanzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c56e6-127">The instance resource id</span></span>

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

### <span data-ttu-id="c56e6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56e6-128">-ResourceGroupName</span></span>
<span data-ttu-id="c56e6-129">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c56e6-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="c56e6-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c56e6-130">-Confirm</span></span>
<span data-ttu-id="c56e6-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c56e6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56e6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56e6-132">-WhatIf</span></span>
<span data-ttu-id="c56e6-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c56e6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56e6-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c56e6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56e6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56e6-135">CommonParameters</span></span>
<span data-ttu-id="c56e6-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56e6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56e6-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c56e6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56e6-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c56e6-138">INPUTS</span></span>

### <span data-ttu-id="c56e6-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c56e6-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="c56e6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c56e6-140">System.String</span></span>

## <span data-ttu-id="c56e6-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c56e6-141">OUTPUTS</span></span>

### <span data-ttu-id="c56e6-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="c56e6-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="c56e6-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c56e6-143">NOTES</span></span>

## <span data-ttu-id="c56e6-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c56e6-144">RELATED LINKS</span></span>
