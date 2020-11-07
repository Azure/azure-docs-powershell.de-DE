---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: b1f4b8d53a1031cef76d51a87bbf9afa5b75758f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664453"
---
# <span data-ttu-id="e8406-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e8406-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="e8406-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8406-102">SYNOPSIS</span></span>
<span data-ttu-id="e8406-103">Entfernt eine Anmeldeinformationen von einem Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="e8406-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8406-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8406-104">SYNTAX</span></span>

### <span data-ttu-id="e8406-105">ObjectIdWithKeyIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8406-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8406-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8406-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8406-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8406-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8406-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8406-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8406-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8406-109">DESCRIPTION</span></span>
<span data-ttu-id="e8406-110">Das Remove-AzureRmADSpCredential-Cmdlet kann verwendet werden, um einen Anmeldeinformationsschlüssel aus einem Dienstprinzipal zu entfernen, wenn es sich um einen Kompromiss handelt oder als Teil des Rollover-Ablaufs des Anmeldeinformationsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="e8406-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="e8406-111">Der Dienstprinzipal wird identifiziert, indem entweder die Objekt-ID oder der Dienstprinzipalname (Service Principal Name, SPN) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e8406-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="e8406-112">Die zu entfernenden Anmeldeinformationen werden durch die Schlüssel-ID identifiziert, wenn einzelne Anmeldeinformationen entfernt werden sollen, oder mit einem Schalter "alle", um alle dem Dienstprinzipal zugeordneten Anmeldeinformationen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e8406-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="e8406-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8406-113">EXAMPLES</span></span>

### <span data-ttu-id="e8406-114">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e8406-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="e8406-115">Mit diesem Befehl wird ein Anmeldeinformationsschlüssel aus einem Dienstprinzipal entfernt.</span><span class="sxs-lookup"><span data-stu-id="e8406-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="e8406-116">In diesem Beispiel wird der Schlüssel mit der ID "9044423a-60a3-45ac-9ab1-09534157ebb" aus dem Dienstprinzipal entfernt.</span><span class="sxs-lookup"><span data-stu-id="e8406-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="e8406-117">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e8406-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="e8406-118">Mit diesem Befehl wird ein Anmeldeinformationsschlüssel aus einem Dienstprinzipal entfernt.</span><span class="sxs-lookup"><span data-stu-id="e8406-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="e8406-119">In diesem Beispiel werden alle Anmeldeinformationen aus dem Dienstprinzipal entfernt, der dem Dienstprinzipalnamen "" zugeordnet ist http://test123 .</span><span class="sxs-lookup"><span data-stu-id="e8406-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="e8406-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8406-120">PARAMETERS</span></span>

### <span data-ttu-id="e8406-121">– Alle</span><span class="sxs-lookup"><span data-stu-id="e8406-121">-All</span></span>
<span data-ttu-id="e8406-122">Wechseln Sie, um alle Anmeldeinformationen zu entfernen, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e8406-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8406-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e8406-123">-Force</span></span>
<span data-ttu-id="e8406-124">Wechseln Sie, um die Anmeldeinformationen ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e8406-124">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="e8406-125">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e8406-125">-KeyId</span></span>
<span data-ttu-id="e8406-126">Gibt den Anmeldeinformationsschlüssel an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8406-126">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="e8406-127">Die Schlüssel-IDs für einen Dienstprinzipal können mit dem Get-AzureRmADSpCredential-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e8406-127">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8406-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e8406-128">-ObjectId</span></span>
<span data-ttu-id="e8406-129">Die Objekt-ID des Dienst Prinzipals, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8406-129">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8406-130">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e8406-130">-ServicePrincipalName</span></span>
<span data-ttu-id="e8406-131">Der Name (SPN) des Dienst Prinzipals, aus dem die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8406-131">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8406-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8406-132">-Confirm</span></span>
<span data-ttu-id="e8406-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8406-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8406-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8406-134">-WhatIf</span></span>
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

### <span data-ttu-id="e8406-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8406-135">-DefaultProfile</span></span>
<span data-ttu-id="e8406-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8406-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8406-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8406-137">CommonParameters</span></span>
<span data-ttu-id="e8406-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8406-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8406-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8406-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8406-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8406-140">INPUTS</span></span>

## <span data-ttu-id="e8406-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8406-141">OUTPUTS</span></span>

## <span data-ttu-id="e8406-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8406-142">NOTES</span></span>

## <span data-ttu-id="e8406-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8406-143">RELATED LINKS</span></span>

[<span data-ttu-id="e8406-144">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e8406-144">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="e8406-145">Neu – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e8406-145">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="e8406-146">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e8406-146">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

