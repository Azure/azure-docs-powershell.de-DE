---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 94a6b1ed2d02e3072a23ccc82fc4a49149b2ae2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843292"
---
# <span data-ttu-id="7013f-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7013f-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="7013f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7013f-102">SYNOPSIS</span></span>
<span data-ttu-id="7013f-103">Entfernt Anmeldeinformationen aus einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7013f-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="7013f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7013f-104">SYNTAX</span></span>

### <span data-ttu-id="7013f-105">ApplicationObjectIdWithKeyIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7013f-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7013f-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7013f-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7013f-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7013f-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7013f-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7013f-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7013f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7013f-109">DESCRIPTION</span></span>
<span data-ttu-id="7013f-110">Das Remove-AzADAppCredential-Cmdlet kann verwendet werden, um einen Anmeldeinformationsschlüssel aus einer Anwendung im Fall einer Gefährdung oder als Teil des Rollover-Ablaufs von Anmeldeinformationen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7013f-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="7013f-111">Die Anwendung wird identifiziert, indem entweder die Objekt-ID oder die Anwendungs-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7013f-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="7013f-112">Die zu entfernende Anmeldeinformationen werden durch die Schlüssel-ID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7013f-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="7013f-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7013f-113">EXAMPLES</span></span>

### <span data-ttu-id="7013f-114">Beispiel 1: Entfernen bestimmter Anmeldeinformationen aus einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="7013f-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="7013f-115">Entfernt die Anmeldeinformationen mit der Schlüssel-ID "9044423a-60a3-45ac-9ab1-09534157ebb" aus der Anwendung mit der Objekt-ID "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="7013f-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="7013f-116">Beispiel 2 – Entfernen aller Anmeldeinformationen aus einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="7013f-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="7013f-117">Entfernt alle Anmeldeinformationen aus der Anwendung mit der Anwendungs-ID "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="7013f-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="7013f-118">Beispiel 3: Entfernen aller Anmeldeinformationen mithilfe der Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="7013f-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="7013f-119">Ruft die Anwendung mit der Objekt-ID "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82" und Pipes ab, die dem Remove-AzADAppCredential-Cmdlet zugeordnet sind, und entfernt alle Anmeldeinformationen aus dieser Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7013f-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="7013f-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7013f-120">PARAMETERS</span></span>

### <span data-ttu-id="7013f-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7013f-121">-ApplicationId</span></span>
<span data-ttu-id="7013f-122">Die ID der Anwendung, aus der die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7013f-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="7013f-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7013f-123">-ApplicationObject</span></span>
<span data-ttu-id="7013f-124">Das Application-Objekt, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7013f-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7013f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7013f-125">-DefaultProfile</span></span>
<span data-ttu-id="7013f-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7013f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7013f-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7013f-127">-DisplayName</span></span>
<span data-ttu-id="7013f-128">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7013f-128">The display name of the application.</span></span>

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

### <span data-ttu-id="7013f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="7013f-129">-Force</span></span>
<span data-ttu-id="7013f-130">Wechseln Sie, um die Anmeldeinformationen ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7013f-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="7013f-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7013f-131">-KeyId</span></span>
<span data-ttu-id="7013f-132">Gibt den Anmeldeinformationsschlüssel an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7013f-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="7013f-133">Die Schlüssel-IDs für die Anwendung können mit dem Get-AzADAppCredential-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7013f-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="7013f-134">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="7013f-134">-ObjectId</span></span>
<span data-ttu-id="7013f-135">Die Objekt-ID der Anwendung, aus der die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7013f-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7013f-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7013f-136">-PassThru</span></span>
<span data-ttu-id="7013f-137">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7013f-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7013f-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7013f-138">-Confirm</span></span>
<span data-ttu-id="7013f-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7013f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7013f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7013f-140">-WhatIf</span></span>
<span data-ttu-id="7013f-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7013f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7013f-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7013f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7013f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7013f-143">CommonParameters</span></span>
<span data-ttu-id="7013f-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7013f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7013f-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7013f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7013f-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7013f-146">INPUTS</span></span>

### <span data-ttu-id="7013f-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7013f-147">System.Guid</span></span>

### <span data-ttu-id="7013f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7013f-148">System.String</span></span>

### <span data-ttu-id="7013f-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7013f-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="7013f-150">Parameter: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7013f-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="7013f-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7013f-151">OUTPUTS</span></span>

### <span data-ttu-id="7013f-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7013f-152">System.Boolean</span></span>

## <span data-ttu-id="7013f-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="7013f-153">NOTES</span></span>

## <span data-ttu-id="7013f-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7013f-154">RELATED LINKS</span></span>

[<span data-ttu-id="7013f-155">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7013f-155">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="7013f-156">Neu – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7013f-156">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="7013f-157">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7013f-157">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
