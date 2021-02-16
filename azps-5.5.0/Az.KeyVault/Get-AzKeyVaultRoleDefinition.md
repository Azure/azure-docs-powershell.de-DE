---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: 6e4f58c355296a281a9ecbef21d7eca754bf41c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155396"
---
# <span data-ttu-id="bfbb3-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bfbb3-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="bfbb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfbb3-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbb3-103">Listen Sie Rollendefinitionen eines bestimmten verwalteten HSM in einem bestimmten Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="bfbb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfbb3-104">SYNTAX</span></span>

### <span data-ttu-id="bfbb3-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="bfbb3-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfbb3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bfbb3-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfbb3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfbb3-107">DESCRIPTION</span></span>
<span data-ttu-id="bfbb3-108">Listen Sie Rollendefinitionen eines bestimmten verwalteten HSM in einem bestimmten Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="bfbb3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bfbb3-109">EXAMPLES</span></span>

### <span data-ttu-id="bfbb3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bfbb3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="bfbb3-111">Im Beispiel werden alle Rollen im Bereich "/schlüssel" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="bfbb3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bfbb3-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="bfbb3-113">Das Beispiel ruft die Rolle "Verwaltete HSM-Sicherung" ab und überprüft deren Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="bfbb3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfbb3-114">PARAMETERS</span></span>

### <span data-ttu-id="bfbb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbb3-115">-DefaultProfile</span></span>
<span data-ttu-id="bfbb3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfbb3-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="bfbb3-117">-HsmName</span></span>
<span data-ttu-id="bfbb3-118">Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-118">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfbb3-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bfbb3-119">-RoleDefinitionName</span></span>
<span data-ttu-id="bfbb3-120">Der Name der rollendefinition, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfbb3-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="bfbb3-121">-Scope</span></span>
<span data-ttu-id="bfbb3-122">Bereich, für den die Rollenzuweisung oder -definition gilt, z. B. '/' oder '/keys' oder '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="bfbb3-123">Bei Ausgelassen wird "/" verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-123">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfbb3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbb3-124">CommonParameters</span></span>
<span data-ttu-id="bfbb3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfbb3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbb3-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfbb3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbb3-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bfbb3-127">INPUTS</span></span>

### <span data-ttu-id="bfbb3-128">Keine</span><span class="sxs-lookup"><span data-stu-id="bfbb3-128">None</span></span>

## <span data-ttu-id="bfbb3-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bfbb3-129">OUTPUTS</span></span>

### <span data-ttu-id="bfbb3-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bfbb3-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="bfbb3-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bfbb3-131">NOTES</span></span>

## <span data-ttu-id="bfbb3-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bfbb3-132">RELATED LINKS</span></span>
