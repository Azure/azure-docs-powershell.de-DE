---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 0fa6dde8584eb003bd479e9a73ec96176282d83c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659561"
---
# <span data-ttu-id="e3f4b-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3f4b-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="e3f4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f4b-103">Löscht den Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="e3f4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3f4b-104">SYNTAX</span></span>

### <span data-ttu-id="e3f4b-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3f4b-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f4b-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f4b-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f4b-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f4b-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f4b-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f4b-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f4b-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f4b-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f4b-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f4b-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3f4b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3f4b-111">DESCRIPTION</span></span>
<span data-ttu-id="e3f4b-112">Löscht den Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="e3f4b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3f4b-113">EXAMPLES</span></span>

### <span data-ttu-id="e3f4b-114">Beispiel 1: Entfernen eines Dienst Prinzipals nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="e3f4b-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="e3f4b-115">Entfernt den Dienstprinzipal mit der Objekt-ID "61b5d8ea-fdc6-40A2-8d5b-ad447c678d45".</span><span class="sxs-lookup"><span data-stu-id="e3f4b-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="e3f4b-116">Beispiel 2 – Entfernen eines Dienst Prinzipals nach Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="e3f4b-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="e3f4b-117">Entfernt den Dienstprinzipal mit der Anwendungs-ID "9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="e3f4b-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="e3f4b-118">Beispiel 3: Entfernen eines Dienst Prinzipals nach SPN</span><span class="sxs-lookup"><span data-stu-id="e3f4b-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="e3f4b-119">Entfernen des Dienst Prinzipals mit dem Dienstprinzipalnamen "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="e3f4b-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="e3f4b-120">Beispiel 4 – Entfernen eines Dienst Prinzipals durch Piping</span><span class="sxs-lookup"><span data-stu-id="e3f4b-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="e3f4b-121">Ruft den Dienstprinzipal mit der Objekt-ID ' 61b5d8ea-fdc6-40A2-8d5b-ad447c678d45 ' und Pipes ab, die zum Remove-AzADServicePrincipal-Cmdlet, um diesen Dienstprinzipal zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="e3f4b-122">Beispiel 5 – Entfernen eines Dienst Prinzipals durch Piping einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="e3f4b-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="e3f4b-123">Ruft die Anwendung mit der Anwendungs-ID "9263469e-d328-4321-8646-3e3e75d20e76" und Pipes ab, die zum Cmdlet Remove-AzADServicePrincipal, um den Dienstprinzipal zu entfernen, der dieser Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="e3f4b-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3f4b-124">PARAMETERS</span></span>

### <span data-ttu-id="e3f4b-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e3f4b-125">-ApplicationId</span></span>
<span data-ttu-id="e3f4b-126">Die Anwendungs-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-126">The service principal application id.</span></span>

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

### <span data-ttu-id="e3f4b-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="e3f4b-127">-ApplicationObject</span></span>
<span data-ttu-id="e3f4b-128">Das Application-Objekt, dessen Dienstprinzipal entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f4b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f4b-129">-DefaultProfile</span></span>
<span data-ttu-id="e3f4b-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e3f4b-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3f4b-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e3f4b-131">-DisplayName</span></span>
<span data-ttu-id="e3f4b-132">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f4b-133">-Force</span><span class="sxs-lookup"><span data-stu-id="e3f4b-133">-Force</span></span>
<span data-ttu-id="e3f4b-134">Wechseln Sie zum Löschen des Dienst Prinzipals, ohne eine Bestätigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="e3f4b-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e3f4b-135">-InputObject</span></span>
<span data-ttu-id="e3f4b-136">Das Dienstprinzipal Objekt.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f4b-137">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e3f4b-137">-ObjectId</span></span>
<span data-ttu-id="e3f4b-138">Die Objekt-ID des Dienst Prinzipals, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f4b-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3f4b-139">-PassThru</span></span>
<span data-ttu-id="e3f4b-140">Gibt, falls angegeben, den gelöschten Dienstprinzipal zurück.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="e3f4b-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e3f4b-141">-ServicePrincipalName</span></span>
<span data-ttu-id="e3f4b-142">Der Dienstprinzipalname.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f4b-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3f4b-143">-Confirm</span></span>
<span data-ttu-id="e3f4b-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f4b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f4b-145">-WhatIf</span></span>
<span data-ttu-id="e3f4b-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3f4b-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f4b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f4b-148">CommonParameters</span></span>
<span data-ttu-id="e3f4b-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f4b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f4b-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f4b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f4b-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3f4b-151">INPUTS</span></span>

### <span data-ttu-id="e3f4b-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e3f4b-152">System.String</span></span>

### <span data-ttu-id="e3f4b-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e3f4b-153">System.Guid</span></span>

### <span data-ttu-id="e3f4b-154">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3f4b-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="e3f4b-155">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e3f4b-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e3f4b-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3f4b-156">OUTPUTS</span></span>

### <span data-ttu-id="e3f4b-157">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3f4b-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e3f4b-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3f4b-158">NOTES</span></span>
<span data-ttu-id="e3f4b-159">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="e3f4b-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e3f4b-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3f4b-160">RELATED LINKS</span></span>

[<span data-ttu-id="e3f4b-161">Neu – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3f4b-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="e3f4b-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3f4b-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="e3f4b-163">Satz-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3f4b-163">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="e3f4b-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e3f4b-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="e3f4b-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e3f4b-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
