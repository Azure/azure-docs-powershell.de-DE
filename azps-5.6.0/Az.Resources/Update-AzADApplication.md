---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 329620701c4afb52bdebd145ef461c7d311c26a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942099"
---
# <span data-ttu-id="308af-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="308af-101">Update-AzADApplication</span></span>

## <span data-ttu-id="308af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="308af-102">SYNOPSIS</span></span>
<span data-ttu-id="308af-103">Aktualisiert eine vorhandene Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="308af-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="308af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="308af-104">SYNTAX</span></span>

### <span data-ttu-id="308af-105">ApplicationObjectIdWithUpdateParamsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="308af-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="308af-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="308af-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="308af-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="308af-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="308af-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="308af-108">DESCRIPTION</span></span>
<span data-ttu-id="308af-109">Aktualisiert eine vorhandene Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="308af-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="308af-110">Zum Aktualisieren der anmeldeinformationen, die dieser Anwendung zugeordnet sind, verwenden Sie bitte das New-AzADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="308af-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="308af-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="308af-111">EXAMPLES</span></span>

### <span data-ttu-id="308af-112">Beispiel 1 : Aktualisieren des Anzeigenamens einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="308af-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="308af-113">Aktualisiert den Anzeigenamen der Anwendung mit der Objekt-ID "fb7b3405-ca44-4b5b-8584-12392f5d96d7" in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="308af-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="308af-114">Beispiel 2 : Aktualisieren aller Eigenschaften einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="308af-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="308af-115">Aktualisiert die Eigenschaften einer Anwendung mit der Objekt-ID "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="308af-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="308af-116">Beispiel 3: Aktualisieren des Anzeigenamens einer Anwendung mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="308af-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="308af-117">Ruft die Anwendung mit der Objekt-ID "fb7b3405-ca44-4b5b-8584-12392f5d96d7" ab und gibt diese an das Update-AzADApplication-Cmdlet weiter, um den Anzeigenamen der Anwendung auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="308af-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="308af-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="308af-118">PARAMETERS</span></span>

### <span data-ttu-id="308af-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="308af-119">-ApplicationId</span></span>
<span data-ttu-id="308af-120">Die Anwendungs-ID der zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="308af-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="308af-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="308af-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="308af-122">True, wenn die Anwendung für andere Mandanten freigegeben ist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="308af-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="308af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308af-123">-DefaultProfile</span></span>
<span data-ttu-id="308af-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="308af-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="308af-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="308af-125">-DisplayName</span></span>
<span data-ttu-id="308af-126">Der Anzeigename für die zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="308af-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="308af-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="308af-127">-HomePage</span></span>
<span data-ttu-id="308af-128">Die URL der Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="308af-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="308af-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="308af-129">-IdentifierUri</span></span>
<span data-ttu-id="308af-130">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="308af-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="308af-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="308af-131">-InputObject</span></span>
<span data-ttu-id="308af-132">Das Objekt, das die zu aktualisierende Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="308af-132">The object representing the application to update.</span></span>

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

### <span data-ttu-id="308af-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="308af-133">-ObjectId</span></span>
<span data-ttu-id="308af-134">Die Objekt-ID der zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="308af-134">The object id of the application to update.</span></span>

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

### <span data-ttu-id="308af-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="308af-135">-ReplyUrl</span></span>
<span data-ttu-id="308af-136">Gibt die URLs an, an die Benutzertoken zur Anmeldung gesendet werden, oder die Umleitungs-URIs, an die OAuth 2.0-Autorisierungscodes und Zugriffstoken gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="308af-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="308af-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="308af-137">-Confirm</span></span>
<span data-ttu-id="308af-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="308af-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="308af-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="308af-139">-WhatIf</span></span>
<span data-ttu-id="308af-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="308af-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="308af-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="308af-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="308af-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308af-142">CommonParameters</span></span>
<span data-ttu-id="308af-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308af-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308af-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="308af-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308af-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="308af-145">INPUTS</span></span>

### <span data-ttu-id="308af-146">System.String</span><span class="sxs-lookup"><span data-stu-id="308af-146">System.String</span></span>

### <span data-ttu-id="308af-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="308af-147">System.Guid</span></span>

### <span data-ttu-id="308af-148">Microsoft.Azure.Commands.ActiveDirectory.PSDApplication</span><span class="sxs-lookup"><span data-stu-id="308af-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="308af-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="308af-149">System.String[]</span></span>

### <span data-ttu-id="308af-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="308af-150">System.Boolean</span></span>

## <span data-ttu-id="308af-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="308af-151">OUTPUTS</span></span>

### <span data-ttu-id="308af-152">Microsoft.Azure.Commands.ActiveDirectory.PSDApplication</span><span class="sxs-lookup"><span data-stu-id="308af-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="308af-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="308af-153">NOTES</span></span>

## <span data-ttu-id="308af-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="308af-154">RELATED LINKS</span></span>
