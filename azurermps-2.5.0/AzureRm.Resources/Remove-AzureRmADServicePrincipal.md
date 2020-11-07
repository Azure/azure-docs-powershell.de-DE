---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 462acabd83090a893119d94d93fd767907c5144b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848092"
---
# <span data-ttu-id="1d083-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1d083-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="1d083-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d083-102">SYNOPSIS</span></span>
<span data-ttu-id="1d083-103">Löscht den Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="1d083-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d083-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d083-104">SYNTAX</span></span>

### <span data-ttu-id="1d083-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d083-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d083-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d083-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d083-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d083-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d083-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d083-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d083-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d083-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d083-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d083-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d083-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d083-111">DESCRIPTION</span></span>
<span data-ttu-id="1d083-112">Löscht den Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="1d083-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="1d083-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d083-113">EXAMPLES</span></span>

### <span data-ttu-id="1d083-114">Beispiel 1: Entfernen eines Dienst Prinzipals nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="1d083-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="1d083-115">Entfernt den Dienstprinzipal mit der Objekt-ID "61b5d8ea-fdc6-40A2-8d5b-ad447c678d45".</span><span class="sxs-lookup"><span data-stu-id="1d083-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="1d083-116">Beispiel 2 – Entfernen eines Dienst Prinzipals nach Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="1d083-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="1d083-117">Entfernt den Dienstprinzipal mit der Anwendungs-ID "9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="1d083-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="1d083-118">Beispiel 3: Entfernen eines Dienst Prinzipals nach SPN</span><span class="sxs-lookup"><span data-stu-id="1d083-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="1d083-119">Entfernen des Dienst Prinzipals mit dem Dienstprinzipalnamen "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="1d083-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="1d083-120">Beispiel 4 – Entfernen eines Dienst Prinzipals durch Piping</span><span class="sxs-lookup"><span data-stu-id="1d083-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="1d083-121">Ruft den Dienstprinzipal mit der Objekt-ID ' 61b5d8ea-fdc6-40A2-8d5b-ad447c678d45 ' und Pipes ab, die zum Remove-AzureRmADServicePrincipal-Cmdlet, um diesen Dienstprinzipal zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="1d083-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="1d083-122">Beispiel 5 – Entfernen eines Dienst Prinzipals durch Piping einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="1d083-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="1d083-123">Ruft die Anwendung mit der Anwendungs-ID "9263469e-d328-4321-8646-3e3e75d20e76" und Pipes ab, die zum Cmdlet Remove-AzureRmADServicePrincipal, um den Dienstprinzipal zu entfernen, der dieser Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1d083-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="1d083-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d083-124">PARAMETERS</span></span>

### <span data-ttu-id="1d083-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1d083-125">-ApplicationId</span></span>
<span data-ttu-id="1d083-126">Die Anwendungs-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="1d083-126">The service principal application id.</span></span>

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

### <span data-ttu-id="1d083-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="1d083-127">-ApplicationObject</span></span>
<span data-ttu-id="1d083-128">Das Application-Objekt, dessen Dienstprinzipal entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1d083-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d083-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d083-129">-DefaultProfile</span></span>
<span data-ttu-id="1d083-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1d083-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d083-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1d083-131">-DisplayName</span></span>
<span data-ttu-id="1d083-132">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="1d083-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="1d083-133">-Force</span><span class="sxs-lookup"><span data-stu-id="1d083-133">-Force</span></span>
<span data-ttu-id="1d083-134">Wechseln Sie zum Löschen des Dienst Prinzipals, ohne eine Bestätigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1d083-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="1d083-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1d083-135">-InputObject</span></span>
<span data-ttu-id="1d083-136">Das Dienstprinzipal Objekt.</span><span class="sxs-lookup"><span data-stu-id="1d083-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d083-137">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="1d083-137">-ObjectId</span></span>
<span data-ttu-id="1d083-138">Die Objekt-ID des Dienst Prinzipals, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d083-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d083-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d083-139">-PassThru</span></span>
<span data-ttu-id="1d083-140">Gibt, falls angegeben, den gelöschten Dienstprinzipal zurück.</span><span class="sxs-lookup"><span data-stu-id="1d083-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="1d083-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1d083-141">-ServicePrincipalName</span></span>
<span data-ttu-id="1d083-142">Der Dienstprinzipalname.</span><span class="sxs-lookup"><span data-stu-id="1d083-142">The service principal name.</span></span>

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

### <span data-ttu-id="1d083-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d083-143">-Confirm</span></span>
<span data-ttu-id="1d083-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d083-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d083-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d083-145">-WhatIf</span></span>
<span data-ttu-id="1d083-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d083-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d083-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d083-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d083-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d083-148">CommonParameters</span></span>
<span data-ttu-id="1d083-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d083-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d083-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d083-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d083-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d083-151">INPUTS</span></span>

### <span data-ttu-id="1d083-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1d083-152">System.Guid</span></span>

### <span data-ttu-id="1d083-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1d083-153">System.String</span></span>

### <span data-ttu-id="1d083-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1d083-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="1d083-155">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d083-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1d083-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1d083-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="1d083-157">Parameter: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d083-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="1d083-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d083-158">OUTPUTS</span></span>

### <span data-ttu-id="1d083-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1d083-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="1d083-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d083-160">NOTES</span></span>
<span data-ttu-id="1d083-161">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="1d083-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1d083-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d083-162">RELATED LINKS</span></span>

[<span data-ttu-id="1d083-163">Neu – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1d083-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1d083-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1d083-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



[<span data-ttu-id="1d083-165">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1d083-165">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="1d083-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1d083-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
