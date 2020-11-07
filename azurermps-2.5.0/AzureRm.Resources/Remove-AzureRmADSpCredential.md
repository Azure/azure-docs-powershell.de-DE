---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 73fff5ff4cf612c39bacd26fed61c4e856e34128
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848099"
---
# <span data-ttu-id="55757-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="55757-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="55757-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55757-102">SYNOPSIS</span></span>
<span data-ttu-id="55757-103">Entfernt eine Anmeldeinformationen von einem Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="55757-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55757-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55757-104">SYNTAX</span></span>

### <span data-ttu-id="55757-105">ObjectIdWithKeyIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55757-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55757-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55757-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55757-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55757-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55757-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55757-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55757-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55757-109">DESCRIPTION</span></span>
<span data-ttu-id="55757-110">Das Remove-AzureRmADSpCredential-Cmdlet kann verwendet werden, um einen Anmeldeinformationsschlüssel aus einem Dienstprinzipal zu entfernen, wenn es sich um einen Kompromiss handelt oder als Teil des Rollover-Ablaufs des Anmeldeinformationsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="55757-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="55757-111">Der Dienstprinzipal wird identifiziert, indem entweder die Objekt-ID oder der Dienstprinzipalname (Service Principal Name, SPN) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="55757-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="55757-112">Die zu entfernenden Anmeldeinformationen werden durch die Schlüssel-ID identifiziert, wenn einzelne Anmeldeinformationen entfernt werden sollen, oder mit einem Schalter "alle", um alle dem Dienstprinzipal zugeordneten Anmeldeinformationen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="55757-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="55757-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55757-113">EXAMPLES</span></span>

### <span data-ttu-id="55757-114">Beispiel 1: Entfernen einer bestimmten Anmeldeinformationen von einem Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="55757-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="55757-115">Entfernt die Anmeldeinformationen mit der Schlüssel-ID "9044423a-60a3-45ac-9ab1-09534157ebb" aus dem Dienstprinzipal mit der Objekt-ID "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="55757-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="55757-116">Beispiel 2 – Entfernen aller Anmeldeinformationen eines Dienst Prinzipals</span><span class="sxs-lookup"><span data-stu-id="55757-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="55757-117">Entfernt alle Anmeldeinformationen aus dem Dienstprinzipal mit dem SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="55757-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="55757-118">Beispiel 3: Entfernen aller Anmeldeinformationen von einem Dienstprinzipal mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="55757-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADSpCredential
```

<span data-ttu-id="55757-119">Ruft den Dienstprinzipal mit der Objekt-ID "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82" und Pipes ab, die zum Cmdlet Remove-AzureRmADSpCredential, um alle Anmeldeinformationen aus diesem Dienstprinzipal zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="55757-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="55757-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="55757-120">PARAMETERS</span></span>

### <span data-ttu-id="55757-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55757-121">-DefaultProfile</span></span>
<span data-ttu-id="55757-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="55757-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55757-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55757-123">-DisplayName</span></span>
<span data-ttu-id="55757-124">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="55757-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55757-125">-Force</span><span class="sxs-lookup"><span data-stu-id="55757-125">-Force</span></span>
<span data-ttu-id="55757-126">Wechseln Sie, um die Anmeldeinformationen ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="55757-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="55757-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="55757-127">-KeyId</span></span>
<span data-ttu-id="55757-128">Gibt den Anmeldeinformationsschlüssel an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55757-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="55757-129">Die Schlüssel-IDs für einen Dienstprinzipal können mit dem Get-AzureRmADSpCredential-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="55757-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55757-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="55757-130">-ObjectId</span></span>
<span data-ttu-id="55757-131">Die Objekt-ID des Dienst Prinzipals, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55757-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55757-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55757-132">-PassThru</span></span>
<span data-ttu-id="55757-133">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="55757-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="55757-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="55757-134">-ServicePrincipalName</span></span>
<span data-ttu-id="55757-135">Der Name (SPN) des Dienst Prinzipals, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55757-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55757-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="55757-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="55757-137">Das Dienstprinzipal Objekt, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55757-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55757-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55757-138">-Confirm</span></span>
<span data-ttu-id="55757-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55757-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55757-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55757-140">-WhatIf</span></span>
<span data-ttu-id="55757-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55757-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55757-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55757-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55757-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55757-143">CommonParameters</span></span>
<span data-ttu-id="55757-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55757-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55757-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55757-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55757-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55757-146">INPUTS</span></span>

### <span data-ttu-id="55757-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="55757-147">System.Guid</span></span>

### <span data-ttu-id="55757-148">System. String</span><span class="sxs-lookup"><span data-stu-id="55757-148">System.String</span></span>

### <span data-ttu-id="55757-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="55757-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="55757-150">Parameter: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="55757-150">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="55757-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55757-151">OUTPUTS</span></span>

### <span data-ttu-id="55757-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55757-152">System.Boolean</span></span>

## <span data-ttu-id="55757-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="55757-153">NOTES</span></span>

## <span data-ttu-id="55757-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55757-154">RELATED LINKS</span></span>

[<span data-ttu-id="55757-155">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="55757-155">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="55757-156">Neu – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="55757-156">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="55757-157">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="55757-157">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

