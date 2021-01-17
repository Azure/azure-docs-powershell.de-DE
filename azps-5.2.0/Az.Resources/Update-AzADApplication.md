---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302691"
---
# <span data-ttu-id="9174b-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9174b-101">Update-AzADApplication</span></span>

## <span data-ttu-id="9174b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9174b-102">SYNOPSIS</span></span>
<span data-ttu-id="9174b-103">Aktualisiert eine vorhandene Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9174b-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="9174b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9174b-104">SYNTAX</span></span>

### <span data-ttu-id="9174b-105">ApplicationObjectIdWithUpdateParamsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9174b-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9174b-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="9174b-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9174b-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="9174b-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9174b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9174b-108">DESCRIPTION</span></span>
<span data-ttu-id="9174b-109">Aktualisiert eine vorhandene Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9174b-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="9174b-110">Um die Anmeldeinformationen zu aktualisieren, die dieser Anwendung zugeordnet sind, verwenden Sie das New-AzADAppCredential Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9174b-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="9174b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9174b-111">EXAMPLES</span></span>

### <span data-ttu-id="9174b-112">Beispiel 1: Aktualisieren des Anzeigenamens einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="9174b-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="9174b-113">Aktualisiert den Anzeigenamen der Anwendung mit der Objekt-ID 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' in 'MyNewDisplayName'.</span><span class="sxs-lookup"><span data-stu-id="9174b-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="9174b-114">Beispiel 2: Aktualisieren aller Eigenschaften einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="9174b-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="9174b-115">Aktualisiert die Eigenschaften einer Anwendung mit der Objekt-ID 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span><span class="sxs-lookup"><span data-stu-id="9174b-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="9174b-116">Beispiel 3: Aktualisieren des Anzeigenamens einer Anwendung mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="9174b-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="9174b-117">Ruft die Anwendung mit der Objekt-ID 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' ab und gibt diese an das cmdlet Update-AzADApplication weiter, um den Anzeigenamen der Anwendung auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9174b-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="9174b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9174b-118">PARAMETERS</span></span>

### <span data-ttu-id="9174b-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9174b-119">-ApplicationId</span></span>
<span data-ttu-id="9174b-120">Die Anwendungs-ID der zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9174b-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9174b-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="9174b-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="9174b-122">"True", wenn die Anwendung für andere Mandanten freigegeben ist. andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="9174b-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9174b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9174b-123">-DefaultProfile</span></span>
<span data-ttu-id="9174b-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9174b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9174b-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9174b-125">-DisplayName</span></span>
<span data-ttu-id="9174b-126">Der Anzeigename für die zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9174b-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9174b-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="9174b-127">-HomePage</span></span>
<span data-ttu-id="9174b-128">Die URL der Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9174b-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9174b-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="9174b-129">-IdentifierUri</span></span>
<span data-ttu-id="9174b-130">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9174b-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9174b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9174b-131">-InputObject</span></span>
<span data-ttu-id="9174b-132">Das Objekt, das die zu aktualisierende Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="9174b-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9174b-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9174b-133">-ObjectId</span></span>
<span data-ttu-id="9174b-134">Die Objekt-ID der zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9174b-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9174b-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="9174b-135">-ReplyUrl</span></span>
<span data-ttu-id="9174b-136">Gibt die URLs an, an die Benutzertoken zur Anmeldung gesendet werden, oder die Umleitungs-URIs, an die OAuth 2.0-Autorisierungscodes und -Zugriffstoken gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9174b-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9174b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9174b-137">-Confirm</span></span>
<span data-ttu-id="9174b-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9174b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9174b-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9174b-139">-WhatIf</span></span>
<span data-ttu-id="9174b-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9174b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9174b-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9174b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9174b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9174b-142">CommonParameters</span></span>
<span data-ttu-id="9174b-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9174b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9174b-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9174b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9174b-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9174b-145">INPUTS</span></span>

### <span data-ttu-id="9174b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="9174b-146">System.String</span></span>

### <span data-ttu-id="9174b-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9174b-147">System.Guid</span></span>

### <span data-ttu-id="9174b-148">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="9174b-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="9174b-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9174b-149">System.String[]</span></span>

### <span data-ttu-id="9174b-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9174b-150">System.Boolean</span></span>

## <span data-ttu-id="9174b-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9174b-151">OUTPUTS</span></span>

### <span data-ttu-id="9174b-152">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="9174b-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="9174b-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9174b-153">NOTES</span></span>

## <span data-ttu-id="9174b-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9174b-154">RELATED LINKS</span></span>
