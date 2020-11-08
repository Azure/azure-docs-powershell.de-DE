---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: bcb33f87b85eb6ad5bce9ba812ebccb4d154e920
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176088"
---
# <span data-ttu-id="8a5b2-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8a5b2-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="8a5b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a5b2-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5b2-103">Entfernt eine Anmeldeinformationen von einem Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="8a5b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a5b2-104">SYNTAX</span></span>

### <span data-ttu-id="8a5b2-105">ObjectIdWithKeyIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a5b2-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a5b2-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a5b2-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a5b2-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a5b2-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a5b2-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a5b2-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a5b2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a5b2-109">DESCRIPTION</span></span>
<span data-ttu-id="8a5b2-110">Das Remove-AzADSpCredential-Cmdlet kann verwendet werden, um einen Anmeldeinformationsschlüssel aus einem Dienstprinzipal zu entfernen, wenn es sich um einen Kompromiss handelt oder als Teil des Rollover-Ablaufs des Anmeldeinformationsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="8a5b2-111">Der Dienstprinzipal wird identifiziert, indem entweder die Objekt-ID oder der Dienstprinzipalname (Service Principal Name, SPN) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="8a5b2-112">Die zu entfernenden Anmeldeinformationen werden durch die Schlüssel-ID identifiziert, wenn einzelne Anmeldeinformationen entfernt werden sollen, oder mit einem Schalter "alle", um alle dem Dienstprinzipal zugeordneten Anmeldeinformationen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="8a5b2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a5b2-113">EXAMPLES</span></span>

### <span data-ttu-id="8a5b2-114">Beispiel 1: Entfernen einer bestimmten Anmeldeinformationen von einem Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="8a5b2-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="8a5b2-115">Entfernt die Anmeldeinformationen mit der Schlüssel-ID "9044423a-60a3-45ac-9ab1-09534157ebb" aus dem Dienstprinzipal mit der Objekt-ID "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="8a5b2-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="8a5b2-116">Beispiel 2: Entfernen aller Anmeldeinformationen eines Dienst Prinzipals</span><span class="sxs-lookup"><span data-stu-id="8a5b2-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="8a5b2-117">Entfernt alle Anmeldeinformationen aus dem Dienstprinzipal mit dem SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="8a5b2-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="8a5b2-118">Beispiel 3: Entfernen aller Anmeldeinformationen von einem Dienstprinzipal mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="8a5b2-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="8a5b2-119">Ruft den Dienstprinzipal mit der Objekt-ID "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82" und Pipes ab, die zum Cmdlet Remove-AzADSpCredential, um alle Anmeldeinformationen aus diesem Dienstprinzipal zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="8a5b2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a5b2-120">PARAMETERS</span></span>

### <span data-ttu-id="8a5b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5b2-121">-DefaultProfile</span></span>
<span data-ttu-id="8a5b2-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8a5b2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a5b2-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8a5b2-123">-DisplayName</span></span>
<span data-ttu-id="8a5b2-124">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="8a5b2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8a5b2-125">-Force</span></span>
<span data-ttu-id="8a5b2-126">Wechseln Sie, um die Anmeldeinformationen ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="8a5b2-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="8a5b2-127">-KeyId</span></span>
<span data-ttu-id="8a5b2-128">Gibt den Anmeldeinformationsschlüssel an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="8a5b2-129">Die Schlüssel-IDs für einen Dienstprinzipal können mit dem Get-AzADSpCredential-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="8a5b2-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8a5b2-130">-ObjectId</span></span>
<span data-ttu-id="8a5b2-131">Die Objekt-ID des Dienst Prinzipals, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a5b2-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a5b2-132">-PassThru</span></span>
<span data-ttu-id="8a5b2-133">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8a5b2-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a5b2-134">-ServicePrincipalName</span></span>
<span data-ttu-id="8a5b2-135">Der Name (SPN) des Dienst Prinzipals, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="8a5b2-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="8a5b2-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="8a5b2-137">Das Dienstprinzipal Objekt, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a5b2-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a5b2-138">-Confirm</span></span>
<span data-ttu-id="8a5b2-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a5b2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a5b2-140">-WhatIf</span></span>
<span data-ttu-id="8a5b2-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a5b2-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a5b2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5b2-143">CommonParameters</span></span>
<span data-ttu-id="8a5b2-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a5b2-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a5b2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5b2-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a5b2-146">INPUTS</span></span>

### <span data-ttu-id="8a5b2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8a5b2-147">System.String</span></span>

### <span data-ttu-id="8a5b2-148">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8a5b2-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="8a5b2-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8a5b2-149">System.Guid</span></span>

## <span data-ttu-id="8a5b2-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a5b2-150">OUTPUTS</span></span>

### <span data-ttu-id="8a5b2-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a5b2-151">System.Boolean</span></span>

## <span data-ttu-id="8a5b2-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a5b2-152">NOTES</span></span>

## <span data-ttu-id="8a5b2-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a5b2-153">RELATED LINKS</span></span>

[<span data-ttu-id="8a5b2-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8a5b2-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="8a5b2-155">Neu – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8a5b2-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="8a5b2-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8a5b2-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

