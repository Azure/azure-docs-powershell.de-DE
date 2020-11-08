---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
ms.openlocfilehash: 60ba6fbf57fa9e1ac9e25a913fb9755902b56ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175513"
---
# <span data-ttu-id="33b04-101">Get-AzManagedHsmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="33b04-101">Get-AzManagedHsmRoleDefinition</span></span>

## <span data-ttu-id="33b04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33b04-102">SYNOPSIS</span></span>
<span data-ttu-id="33b04-103">Listen Rollendefinitionen für ein bestimmtes verwaltetes HSM in einem bestimmten Bereich.</span><span class="sxs-lookup"><span data-stu-id="33b04-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="33b04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33b04-104">SYNTAX</span></span>

### <span data-ttu-id="33b04-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="33b04-105">Interactive (Default)</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33b04-106">ByName</span><span class="sxs-lookup"><span data-stu-id="33b04-106">ByName</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33b04-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33b04-107">DESCRIPTION</span></span>
<span data-ttu-id="33b04-108">Listen Rollendefinitionen für ein bestimmtes verwaltetes HSM in einem bestimmten Bereich.</span><span class="sxs-lookup"><span data-stu-id="33b04-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="33b04-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33b04-109">EXAMPLES</span></span>

### <span data-ttu-id="33b04-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33b04-110">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleDefinition -HsmName myHsm -Scope "/keys"

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

<span data-ttu-id="33b04-111">Im Beispiel werden alle Rollen im Bereich "/Keys" aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="33b04-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="33b04-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="33b04-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzManagedHsmRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

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

<span data-ttu-id="33b04-113">Im Beispiel wird die Rolle "Managed HSM Backup" abgerufen und deren Berechtigungen überprüft.</span><span class="sxs-lookup"><span data-stu-id="33b04-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="33b04-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="33b04-114">PARAMETERS</span></span>

### <span data-ttu-id="33b04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b04-115">-DefaultProfile</span></span>
<span data-ttu-id="33b04-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33b04-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33b04-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="33b04-117">-HsmName</span></span>
<span data-ttu-id="33b04-118">Der Name des HSM.</span><span class="sxs-lookup"><span data-stu-id="33b04-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="33b04-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="33b04-119">-RoleDefinitionName</span></span>
<span data-ttu-id="33b04-120">Der Name der Rollendefinition, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="33b04-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="33b04-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="33b04-121">-Scope</span></span>
<span data-ttu-id="33b04-122">Der Bereich, für den die Rollenzuweisung oder-Definition gilt, beispielsweise "/" oder "/Keys" oder "/Keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="33b04-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="33b04-123">"/" wird verwendet, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="33b04-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="33b04-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b04-124">CommonParameters</span></span>
<span data-ttu-id="33b04-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b04-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b04-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33b04-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b04-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33b04-127">INPUTS</span></span>

### <span data-ttu-id="33b04-128">Keine</span><span class="sxs-lookup"><span data-stu-id="33b04-128">None</span></span>

## <span data-ttu-id="33b04-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33b04-129">OUTPUTS</span></span>

### <span data-ttu-id="33b04-130">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="33b04-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="33b04-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="33b04-131">NOTES</span></span>

## <span data-ttu-id="33b04-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33b04-132">RELATED LINKS</span></span>
