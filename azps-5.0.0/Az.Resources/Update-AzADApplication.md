---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179362"
---
# <span data-ttu-id="dd3fe-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dd3fe-101">Update-AzADApplication</span></span>

## <span data-ttu-id="dd3fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3fe-103">Aktualisiert eine vorhandene Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="dd3fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd3fe-104">SYNTAX</span></span>

### <span data-ttu-id="dd3fe-105">ApplicationObjectIdWithUpdateParamsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd3fe-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd3fe-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd3fe-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd3fe-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd3fe-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd3fe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd3fe-108">DESCRIPTION</span></span>
<span data-ttu-id="dd3fe-109">Aktualisiert eine vorhandene Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="dd3fe-110">Verwenden Sie das Cmdlet New-AzADAppCredential, um die Anmeldeinformationen zu aktualisieren, die dieser Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="dd3fe-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd3fe-111">EXAMPLES</span></span>

### <span data-ttu-id="dd3fe-112">Beispiel 1 – Aktualisieren des Anzeigenamens einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="dd3fe-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="dd3fe-113">Aktualisiert den Anzeigenamen der Anwendung mit der Objekt-ID "fb7b3405-CA44-4B5B-8584-12392f5d96d7" als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="dd3fe-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="dd3fe-114">Beispiel 2 – Aktualisieren aller Eigenschaften einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="dd3fe-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="dd3fe-115">Aktualisiert die Eigenschaften einer Anwendung mit der Objekt-ID "fb7b3405-CA44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="dd3fe-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="dd3fe-116">Beispiel 3: Aktualisieren des Anzeigenamens einer Anwendung mithilfe der Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="dd3fe-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="dd3fe-117">Ruft die Anwendung mit der Objekt-ID "fb7b3405-CA44-4B5B-8584-12392f5d96d7" und Pipes ab, die dem Update-AzADApplication-Cmdlet zugeordnet sind, um den Anzeigenamen der Anwendung auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="dd3fe-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd3fe-118">PARAMETERS</span></span>

### <span data-ttu-id="dd3fe-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dd3fe-119">-ApplicationId</span></span>
<span data-ttu-id="dd3fe-120">Die Anwendungs-ID der zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="dd3fe-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="dd3fe-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="dd3fe-122">"True", wenn die Anwendung für andere Mandanten freigegeben wird; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="dd3fe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3fe-123">-DefaultProfile</span></span>
<span data-ttu-id="dd3fe-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd3fe-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd3fe-125">-DisplayName</span></span>
<span data-ttu-id="dd3fe-126">Der Anzeigename der Anwendung, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="dd3fe-127">-Startseite</span><span class="sxs-lookup"><span data-stu-id="dd3fe-127">-HomePage</span></span>
<span data-ttu-id="dd3fe-128">Die URL zur Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="dd3fe-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="dd3fe-129">-IdentifierUri</span></span>
<span data-ttu-id="dd3fe-130">Die URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="dd3fe-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd3fe-131">-InputObject</span></span>
<span data-ttu-id="dd3fe-132">Das Objekt, das die zu aktualisierbare Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-132">The object representing the application to update.</span></span>

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

### <span data-ttu-id="dd3fe-133">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="dd3fe-133">-ObjectId</span></span>
<span data-ttu-id="dd3fe-134">Die Objekt-ID der zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-134">The object id of the application to update.</span></span>

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

### <span data-ttu-id="dd3fe-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="dd3fe-135">-ReplyUrl</span></span>
<span data-ttu-id="dd3fe-136">Gibt die URLs an, an die Benutzertoken für die Anmeldung gesendet werden, oder die Redirect-URIs, an die OAuth 2,0-Autorisierungscodes und Zugriffstoken gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="dd3fe-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd3fe-137">-Confirm</span></span>
<span data-ttu-id="dd3fe-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd3fe-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd3fe-139">-WhatIf</span></span>
<span data-ttu-id="dd3fe-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd3fe-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd3fe-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3fe-142">CommonParameters</span></span>
<span data-ttu-id="dd3fe-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd3fe-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3fe-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd3fe-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3fe-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd3fe-145">INPUTS</span></span>

### <span data-ttu-id="dd3fe-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dd3fe-146">System.String</span></span>

### <span data-ttu-id="dd3fe-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dd3fe-147">System.Guid</span></span>

### <span data-ttu-id="dd3fe-148">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="dd3fe-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="dd3fe-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="dd3fe-149">System.String[]</span></span>

### <span data-ttu-id="dd3fe-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd3fe-150">System.Boolean</span></span>

## <span data-ttu-id="dd3fe-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd3fe-151">OUTPUTS</span></span>

### <span data-ttu-id="dd3fe-152">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="dd3fe-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="dd3fe-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd3fe-153">NOTES</span></span>

## <span data-ttu-id="dd3fe-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd3fe-154">RELATED LINKS</span></span>
