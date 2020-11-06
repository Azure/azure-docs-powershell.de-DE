---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 0cfcb2713eaac255f625b09c0ba81883242f48aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478265"
---
# <span data-ttu-id="03ab6-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="03ab6-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="03ab6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="03ab6-103">Entfernt Anmeldeinformationen aus einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="03ab6-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03ab6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03ab6-104">SYNTAX</span></span>

### <span data-ttu-id="03ab6-105">ApplicationObjectIdWithKeyIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="03ab6-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03ab6-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ab6-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03ab6-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ab6-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03ab6-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ab6-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03ab6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03ab6-109">DESCRIPTION</span></span>
<span data-ttu-id="03ab6-110">Das Remove-AzureRmADAppCredential-Cmdlet kann verwendet werden, um einen Anmeldeinformationsschlüssel aus einer Anwendung im Fall einer Gefährdung oder als Teil des Rollover-Ablaufs von Anmeldeinformationen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="03ab6-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="03ab6-111">Die Anwendung wird identifiziert, indem entweder die Objekt-ID oder die Anwendungs-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="03ab6-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="03ab6-112">Die zu entfernenden Anmeldeinformationen werden durch die Schlüssel-ID identifiziert, wenn einzelne Anmeldeinformationen entfernt werden sollen, oder mit einem Schalter "alle", um alle Anmeldeinformationen zu löschen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="03ab6-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="03ab6-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03ab6-113">EXAMPLES</span></span>

### <span data-ttu-id="03ab6-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03ab6-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="03ab6-115">Mit diesem Befehl wird ein Anmeldeinformationsschlüssel aus einer Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ab6-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="03ab6-116">In diesem Beispiel wird der Schlüssel mit der ID "9044423a-60a3-45ac-9ab1-09534157ebb" aus der Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ab6-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="03ab6-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="03ab6-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="03ab6-118">Mit diesem Befehl wird ein Anmeldeinformationsschlüssel aus einer Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ab6-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="03ab6-119">In diesem Beispiel werden alle Anmeldeinformationen aus der Anwendung entfernt, die dem ApplicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="03ab6-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="03ab6-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="03ab6-120">PARAMETERS</span></span>

### <span data-ttu-id="03ab6-121">– Alle</span><span class="sxs-lookup"><span data-stu-id="03ab6-121">-All</span></span>
<span data-ttu-id="03ab6-122">Wechseln Sie, um alle Anmeldeinformationen zu entfernen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="03ab6-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ab6-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="03ab6-123">-ApplicationId</span></span>
<span data-ttu-id="03ab6-124">Die ID der Anwendung, aus der die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="03ab6-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ab6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ab6-125">-DefaultProfile</span></span>
<span data-ttu-id="03ab6-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="03ab6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ab6-127">-Force</span><span class="sxs-lookup"><span data-stu-id="03ab6-127">-Force</span></span>
<span data-ttu-id="03ab6-128">Wechseln Sie, um die Anmeldeinformationen ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="03ab6-128">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ab6-129">-KeyId</span><span class="sxs-lookup"><span data-stu-id="03ab6-129">-KeyId</span></span>
<span data-ttu-id="03ab6-130">Gibt den Anmeldeinformationsschlüssel an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03ab6-130">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="03ab6-131">Die Schlüssel-IDs für die Anwendung können mit dem Get-AzureRmADAppCredential-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="03ab6-131">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ab6-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="03ab6-132">-ObjectId</span></span>
<span data-ttu-id="03ab6-133">Die Objekt-ID der Anwendung, aus der die Anmeldeinformationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="03ab6-133">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ab6-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03ab6-134">-Confirm</span></span>
<span data-ttu-id="03ab6-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03ab6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ab6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ab6-136">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ab6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ab6-137">CommonParameters</span></span>
<span data-ttu-id="03ab6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ab6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ab6-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ab6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ab6-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03ab6-140">INPUTS</span></span>

### <span data-ttu-id="03ab6-141">Keine</span><span class="sxs-lookup"><span data-stu-id="03ab6-141">None</span></span>
<span data-ttu-id="03ab6-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="03ab6-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03ab6-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03ab6-143">OUTPUTS</span></span>

## <span data-ttu-id="03ab6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="03ab6-144">NOTES</span></span>

## <span data-ttu-id="03ab6-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03ab6-145">RELATED LINKS</span></span>

[<span data-ttu-id="03ab6-146">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="03ab6-146">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="03ab6-147">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="03ab6-147">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="03ab6-148">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="03ab6-148">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
