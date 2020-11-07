---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 00c9d6e5a5a729ca5a5119b812873078acb38326
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843291"
---
# <span data-ttu-id="8f058-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f058-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="8f058-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f058-102">SYNOPSIS</span></span>
<span data-ttu-id="8f058-103">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8f058-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="8f058-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f058-104">SYNTAX</span></span>

### <span data-ttu-id="8f058-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f058-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f058-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f058-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f058-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f058-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f058-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f058-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f058-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f058-109">DESCRIPTION</span></span>
<span data-ttu-id="8f058-110">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8f058-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="8f058-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f058-111">EXAMPLES</span></span>

### <span data-ttu-id="8f058-112">Beispiel 1: Entfernen der Anwendung nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="8f058-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="8f058-113">Entfernt die Anwendung mit der Objekt-ID "b4cd1619-80b3-4cfb-9f8f-9f2333425738" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="8f058-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="8f058-114">Beispiel 2 – Entfernen der Anwendung nach Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="8f058-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="8f058-115">Entfernt die Anwendung mit der Anwendungs-ID "f9c5ea4f-28f0-401a-A491-491a037fa346" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="8f058-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="8f058-116">Beispiel 3 – Entfernen der Anwendung durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="8f058-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="8f058-117">Ruft die Anwendung mit der Objekt-ID "b4cd1619-80b3-4cfb-9f8f-9f2333425738" und Pipes ab, die zum Cmdlet Remove-AzADApplication, um die Anwendung aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8f058-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="8f058-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f058-118">PARAMETERS</span></span>

### <span data-ttu-id="8f058-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8f058-119">-ApplicationId</span></span>
<span data-ttu-id="8f058-120">Die Anwendungs-ID der zu entfernenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8f058-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="8f058-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f058-121">-DefaultProfile</span></span>
<span data-ttu-id="8f058-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8f058-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f058-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f058-123">-DisplayName</span></span>
<span data-ttu-id="8f058-124">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8f058-124">The display name of the application.</span></span>

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

### <span data-ttu-id="8f058-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8f058-125">-Force</span></span>
<span data-ttu-id="8f058-126">Wechseln Sie, um eine Anwendung ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8f058-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="8f058-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8f058-127">-InputObject</span></span>
<span data-ttu-id="8f058-128">Das Objekt, das die zu entfernende Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f058-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="8f058-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8f058-129">-ObjectId</span></span>
<span data-ttu-id="8f058-130">Die Objekt-ID der zu löschenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8f058-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="8f058-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f058-131">-PassThru</span></span>
<span data-ttu-id="8f058-132">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8f058-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8f058-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f058-133">-Confirm</span></span>
<span data-ttu-id="8f058-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f058-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f058-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f058-135">-WhatIf</span></span>
<span data-ttu-id="8f058-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f058-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f058-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f058-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f058-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f058-138">CommonParameters</span></span>
<span data-ttu-id="8f058-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f058-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f058-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f058-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f058-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f058-141">INPUTS</span></span>

### <span data-ttu-id="8f058-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8f058-142">System.Guid</span></span>

### <span data-ttu-id="8f058-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8f058-143">System.String</span></span>

### <span data-ttu-id="8f058-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8f058-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="8f058-145">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f058-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8f058-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f058-146">OUTPUTS</span></span>

### <span data-ttu-id="8f058-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f058-147">System.Boolean</span></span>

## <span data-ttu-id="8f058-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f058-148">NOTES</span></span>
<span data-ttu-id="8f058-149">Schlüsselwörter: Azure, AZ, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="8f058-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8f058-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f058-150">RELATED LINKS</span></span>

[<span data-ttu-id="8f058-151">Neu – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f058-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="8f058-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f058-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="8f058-153">Satz-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f058-153">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="8f058-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8f058-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

