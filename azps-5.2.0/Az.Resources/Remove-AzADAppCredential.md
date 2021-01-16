---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: f6344590828663a0cf44d96d6fe733adff8757c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362912"
---
# <span data-ttu-id="fba80-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fba80-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="fba80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba80-102">SYNOPSIS</span></span>
<span data-ttu-id="fba80-103">Entfernt Anmeldeinformationen aus einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fba80-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="fba80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fba80-104">SYNTAX</span></span>

### <span data-ttu-id="fba80-105">ApplicationObjectIdWithKeyIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fba80-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba80-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba80-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba80-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba80-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba80-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba80-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fba80-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fba80-109">DESCRIPTION</span></span>
<span data-ttu-id="fba80-110">Das Remove-AzADAppCredential cmdlet kann verwendet werden, um im Falle eines Kompromisses oder als Teil des Ablaufs des Anmeldeinformationsschlüsselrollovers einen Anmeldeinformationsschlüssel aus einer Anwendung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fba80-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="fba80-111">Die Anwendung wird durch Angabe der Objekt-ID oder der AppId identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fba80-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="fba80-112">Die zu entfernende Anmeldeinformationen werden anhand ihrer Schlüssel-ID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fba80-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="fba80-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fba80-113">EXAMPLES</span></span>

### <span data-ttu-id="fba80-114">Beispiel 1: Entfernen bestimmter Anmeldeinformationen aus einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="fba80-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="fba80-115">Entfernt die Anmeldeinformationen mit der Schlüssel-ID '9044423a-60a3-45ac-9ab1-09534157ebb' aus der Anwendung mit der Objekt-ID '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="fba80-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="fba80-116">Beispiel 2: Entfernen aller Anmeldeinformationen aus einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="fba80-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="fba80-117">Entfernt alle Anmeldeinformationen aus der Anwendung mit der Anwendungs-ID '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="fba80-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="fba80-118">Beispiel 3: Entfernen aller Anmeldeinformationen mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="fba80-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="fba80-119">Ruft die Anwendung mit der Objekt-ID '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' ab und gibt diese an das cmdlet Remove-AzADAppCredential weiter und entfernt alle Anmeldeinformationen aus dieser Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fba80-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="fba80-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fba80-120">PARAMETERS</span></span>

### <span data-ttu-id="fba80-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fba80-121">-ApplicationId</span></span>
<span data-ttu-id="fba80-122">Die ID der Anwendung, aus der die Anmeldeinformationen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="fba80-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="fba80-123">-ApplicationObject</span></span>
<span data-ttu-id="fba80-124">Das Anwendungsobjekt, aus dem die Anmeldeinformationen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="fba80-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba80-125">-DefaultProfile</span></span>
<span data-ttu-id="fba80-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fba80-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fba80-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fba80-127">-DisplayName</span></span>
<span data-ttu-id="fba80-128">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fba80-128">The display name of the application.</span></span>

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

### <span data-ttu-id="fba80-129">-Force</span><span class="sxs-lookup"><span data-stu-id="fba80-129">-Force</span></span>
<span data-ttu-id="fba80-130">Wechseln Sie zum Löschen von Anmeldeinformationen ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="fba80-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="fba80-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="fba80-131">-KeyId</span></span>
<span data-ttu-id="fba80-132">Gibt den zu entfernenden Anmeldeinformationsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="fba80-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="fba80-133">Die Schlüssel-IDs für die Anwendung können mit dem cmdlet Get-AzADAppCredential ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="fba80-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fba80-134">-ObjectId</span></span>
<span data-ttu-id="fba80-135">Die Objekt-ID der Anwendung, aus der die Anmeldeinformationen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="fba80-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fba80-136">-PassThru</span></span>
<span data-ttu-id="fba80-137">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="fba80-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fba80-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fba80-138">-Confirm</span></span>
<span data-ttu-id="fba80-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fba80-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fba80-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fba80-140">-WhatIf</span></span>
<span data-ttu-id="fba80-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fba80-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fba80-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fba80-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fba80-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba80-143">CommonParameters</span></span>
<span data-ttu-id="fba80-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba80-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba80-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fba80-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba80-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fba80-146">INPUTS</span></span>

### <span data-ttu-id="fba80-147">System.String</span><span class="sxs-lookup"><span data-stu-id="fba80-147">System.String</span></span>

### <span data-ttu-id="fba80-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="fba80-148">System.Guid</span></span>

### <span data-ttu-id="fba80-149">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="fba80-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="fba80-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fba80-150">OUTPUTS</span></span>

### <span data-ttu-id="fba80-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fba80-151">System.Boolean</span></span>

## <span data-ttu-id="fba80-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fba80-152">NOTES</span></span>

## <span data-ttu-id="fba80-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fba80-153">RELATED LINKS</span></span>

[<span data-ttu-id="fba80-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fba80-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="fba80-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fba80-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="fba80-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="fba80-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
