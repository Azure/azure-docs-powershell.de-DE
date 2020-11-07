---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 8bcf260156584ddf7c8c2ac0ec347a59214f20c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650637"
---
# <span data-ttu-id="83f3c-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="83f3c-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="83f3c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="83f3c-103">Erstellt eine Registrierungs Definition oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="83f3c-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="83f3c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83f3c-104">SYNTAX</span></span>

### <span data-ttu-id="83f3c-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="83f3c-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f3c-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="83f3c-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f3c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83f3c-107">DESCRIPTION</span></span>
<span data-ttu-id="83f3c-108">Erstellt eine Registrierungs Definition oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="83f3c-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="83f3c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83f3c-109">EXAMPLES</span></span>

### <span data-ttu-id="83f3c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83f3c-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="83f3c-111">Erstellt oder aktualisiert eine Registrierungs Definition, wenn die erforderlichen Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="83f3c-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="83f3c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="83f3c-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="83f3c-113">Erstellt oder aktualisiert eine Registrierungs Definition mit den Plan Details.</span><span class="sxs-lookup"><span data-stu-id="83f3c-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="83f3c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="83f3c-114">PARAMETERS</span></span>

### <span data-ttu-id="83f3c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83f3c-115">-AsJob</span></span>
<span data-ttu-id="83f3c-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="83f3c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83f3c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f3c-117">-DefaultProfile</span></span>
<span data-ttu-id="83f3c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83f3c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83f3c-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83f3c-119">-Description</span></span>
<span data-ttu-id="83f3c-120">Die Beschreibung der Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="83f3c-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="83f3c-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="83f3c-121">-ManagedByTenantId</span></span>
<span data-ttu-id="83f3c-122">Die ManagedBy-Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="83f3c-122">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3c-123">-Planname</span><span class="sxs-lookup"><span data-stu-id="83f3c-123">-PlanName</span></span>
<span data-ttu-id="83f3c-124">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="83f3c-124">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3c-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="83f3c-125">-PlanProduct</span></span>
<span data-ttu-id="83f3c-126">Der Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="83f3c-126">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3c-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="83f3c-127">-PlanPublisher</span></span>
<span data-ttu-id="83f3c-128">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="83f3c-128">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3c-129">-Planversion</span><span class="sxs-lookup"><span data-stu-id="83f3c-129">-PlanVersion</span></span>
<span data-ttu-id="83f3c-130">Die Versionsnummer des Plans.</span><span class="sxs-lookup"><span data-stu-id="83f3c-130">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3c-131">-Prinzipal-Nr</span><span class="sxs-lookup"><span data-stu-id="83f3c-131">-PrincipalId</span></span>
<span data-ttu-id="83f3c-132">Der ManagedBy-Prinzipal Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="83f3c-132">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3c-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="83f3c-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="83f3c-134">Der Name der Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="83f3c-134">The name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3c-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="83f3c-135">-RoleDefinitionId</span></span>
<span data-ttu-id="83f3c-136">Der Rollenbezeichner des verwalteten Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="83f3c-136">The Managed Service Provider's Role Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3c-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83f3c-137">-Confirm</span></span>
<span data-ttu-id="83f3c-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83f3c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f3c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f3c-139">-WhatIf</span></span>
<span data-ttu-id="83f3c-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83f3c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f3c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83f3c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f3c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f3c-142">CommonParameters</span></span>
<span data-ttu-id="83f3c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83f3c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f3c-144">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83f3c-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f3c-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83f3c-145">INPUTS</span></span>

### <span data-ttu-id="83f3c-146">Keine</span><span class="sxs-lookup"><span data-stu-id="83f3c-146">None</span></span>

## <span data-ttu-id="83f3c-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83f3c-147">OUTPUTS</span></span>

### <span data-ttu-id="83f3c-148">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="83f3c-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="83f3c-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="83f3c-149">NOTES</span></span>

## <span data-ttu-id="83f3c-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83f3c-150">RELATED LINKS</span></span>
