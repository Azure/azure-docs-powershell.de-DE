---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: ffebb4e3fca417c896939bb54ed1c0af1c42f7fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845488"
---
# <span data-ttu-id="113d2-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="113d2-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="113d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="113d2-102">SYNOPSIS</span></span>
<span data-ttu-id="113d2-103">Löscht die Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="113d2-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="113d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="113d2-104">SYNTAX</span></span>

### <span data-ttu-id="113d2-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="113d2-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113d2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="113d2-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113d2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="113d2-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="113d2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="113d2-108">DESCRIPTION</span></span>
<span data-ttu-id="113d2-109">Löscht die Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="113d2-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="113d2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="113d2-110">EXAMPLES</span></span>

### <span data-ttu-id="113d2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="113d2-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="113d2-112">Entfernt die Registrierungs Definition mit der angegebenen IT-ID.</span><span class="sxs-lookup"><span data-stu-id="113d2-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="113d2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="113d2-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="113d2-114">Entfernt die Registrierungs Definition, wenn die vollqualifizierte Ressourcen-ID angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="113d2-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="113d2-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="113d2-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="113d2-116">Löscht die Registrierungs Definition, die dem Objekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="113d2-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="113d2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="113d2-117">PARAMETERS</span></span>

### <span data-ttu-id="113d2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="113d2-118">-AsJob</span></span>
<span data-ttu-id="113d2-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="113d2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="113d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="113d2-120">-DefaultProfile</span></span>
<span data-ttu-id="113d2-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="113d2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="113d2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="113d2-122">-Id</span></span>
<span data-ttu-id="113d2-123">Der Bezeichner für die Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="113d2-123">The registration definition identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="113d2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="113d2-124">-InputObject</span></span>
<span data-ttu-id="113d2-125">Das Registrierungs Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="113d2-125">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="113d2-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="113d2-126">-ResourceId</span></span>
<span data-ttu-id="113d2-127">Resourcen der Registrierungs Definition</span><span class="sxs-lookup"><span data-stu-id="113d2-127">ResourceId of the registration definition</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="113d2-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="113d2-128">-Confirm</span></span>
<span data-ttu-id="113d2-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="113d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="113d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="113d2-130">-WhatIf</span></span>
<span data-ttu-id="113d2-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="113d2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="113d2-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="113d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="113d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113d2-133">CommonParameters</span></span>
<span data-ttu-id="113d2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="113d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113d2-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="113d2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113d2-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="113d2-136">INPUTS</span></span>

### <span data-ttu-id="113d2-137">Keine</span><span class="sxs-lookup"><span data-stu-id="113d2-137">None</span></span>

## <span data-ttu-id="113d2-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="113d2-138">OUTPUTS</span></span>

### <span data-ttu-id="113d2-139">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="113d2-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="113d2-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="113d2-140">NOTES</span></span>

## <span data-ttu-id="113d2-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="113d2-141">RELATED LINKS</span></span>
