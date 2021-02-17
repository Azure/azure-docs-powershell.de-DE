---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 956fcf09006e8e65d029bb5e380abc5de0e15c17
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399922"
---
# <span data-ttu-id="45e4b-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="45e4b-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="45e4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="45e4b-103">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="45e4b-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="45e4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45e4b-104">SYNTAX</span></span>

### <span data-ttu-id="45e4b-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="45e4b-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45e4b-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45e4b-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45e4b-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="45e4b-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45e4b-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45e4b-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45e4b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45e4b-109">DESCRIPTION</span></span>
<span data-ttu-id="45e4b-110">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="45e4b-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="45e4b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45e4b-111">EXAMPLES</span></span>

### <span data-ttu-id="45e4b-112">Beispiel 1: Entfernen der Anwendung nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="45e4b-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="45e4b-113">Entfernt die Anwendung mit der Objekt-ID 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="45e4b-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="45e4b-114">Beispiel 2: Entfernen einer Anwendung nach Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="45e4b-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="45e4b-115">Entfernt die Anwendung mit der Anwendungs-ID 'f9c5ea4f-28f0-401a-a491-491a037fa346' aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="45e4b-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="45e4b-116">Beispiel 3: Entfernen der Anwendung durch Piping</span><span class="sxs-lookup"><span data-stu-id="45e4b-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="45e4b-117">Ruft die Anwendung mit der Objekt-ID 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' ab und gibt diese an das Cmdlet Remove-AzADApplication weiter, um die Anwendung aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="45e4b-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="45e4b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45e4b-118">PARAMETERS</span></span>

### <span data-ttu-id="45e4b-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="45e4b-119">-ApplicationId</span></span>
<span data-ttu-id="45e4b-120">Die Anwendungs-ID der zu entfernende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="45e4b-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e4b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e4b-121">-DefaultProfile</span></span>
<span data-ttu-id="45e4b-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="45e4b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e4b-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="45e4b-123">-DisplayName</span></span>
<span data-ttu-id="45e4b-124">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="45e4b-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e4b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="45e4b-125">-Force</span></span>
<span data-ttu-id="45e4b-126">Wechseln Sie zum Löschen einer Anwendung ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="45e4b-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="45e4b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45e4b-127">-InputObject</span></span>
<span data-ttu-id="45e4b-128">Das Objekt, das die zu entfernende Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="45e4b-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45e4b-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="45e4b-129">-ObjectId</span></span>
<span data-ttu-id="45e4b-130">Die Objekt-ID der zu löschende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="45e4b-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e4b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45e4b-131">-PassThru</span></span>
<span data-ttu-id="45e4b-132">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="45e4b-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="45e4b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45e4b-133">-Confirm</span></span>
<span data-ttu-id="45e4b-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45e4b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e4b-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="45e4b-135">-WhatIf</span></span>
<span data-ttu-id="45e4b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45e4b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45e4b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45e4b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e4b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e4b-138">CommonParameters</span></span>
<span data-ttu-id="45e4b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e4b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e4b-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e4b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e4b-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45e4b-141">INPUTS</span></span>

### <span data-ttu-id="45e4b-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="45e4b-142">System.Guid</span></span>

### <span data-ttu-id="45e4b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="45e4b-143">System.String</span></span>

### <span data-ttu-id="45e4b-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="45e4b-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="45e4b-145">Parameter: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45e4b-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="45e4b-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45e4b-146">OUTPUTS</span></span>

### <span data-ttu-id="45e4b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45e4b-147">System.Boolean</span></span>

## <span data-ttu-id="45e4b-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45e4b-148">NOTES</span></span>
<span data-ttu-id="45e4b-149">Schlüsselwörter: azure, Az, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="45e4b-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="45e4b-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45e4b-150">RELATED LINKS</span></span>

[<span data-ttu-id="45e4b-151">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="45e4b-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="45e4b-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="45e4b-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


[<span data-ttu-id="45e4b-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="45e4b-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

