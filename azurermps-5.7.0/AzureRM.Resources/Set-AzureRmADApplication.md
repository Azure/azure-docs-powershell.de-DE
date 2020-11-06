---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: a8c1aa2d0f22a9c6dc6260384e51140cb930106a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502469"
---
# <span data-ttu-id="49d4c-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="49d4c-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="49d4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="49d4c-103">Aktualisiert eine vorhandene Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="49d4c-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49d4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49d4c-104">SYNTAX</span></span>

### <span data-ttu-id="49d4c-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="49d4c-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49d4c-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="49d4c-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49d4c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49d4c-107">DESCRIPTION</span></span>
<span data-ttu-id="49d4c-108">Aktualisiert eine vorhandene Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="49d4c-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="49d4c-109">Verwenden Sie New-AzureRmADAppCredential-Cmdlet, um die Anmeldeinformationen zu aktualisieren, die dieser Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="49d4c-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="49d4c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49d4c-110">EXAMPLES</span></span>

### <span data-ttu-id="49d4c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49d4c-111">Example 1</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="49d4c-112">Aktualisiert die Eigenschaften einer vorhandenen Azure Active Directory-Anwendung mit ObjectID "fb7b3405-CA44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="49d4c-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="49d4c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="49d4c-113">Example 2</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="49d4c-114">Aktualisiert den Anzeigenamen einer vorhandenen Azure Active Directory-Anwendung mit ObjectID "fb7b3405-CA44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="49d4c-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="49d4c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="49d4c-115">PARAMETERS</span></span>

### <span data-ttu-id="49d4c-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="49d4c-116">-ApplicationId</span></span>
<span data-ttu-id="49d4c-117">Die ID der zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="49d4c-117">The id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d4c-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="49d4c-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="49d4c-119">Der Wert, der angibt, ob die Anwendung auf einen einzelnen Mandanten oder einen Mandanten mit mehreren Mandanten aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="49d4c-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d4c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d4c-120">-DefaultProfile</span></span>
<span data-ttu-id="49d4c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="49d4c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49d4c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49d4c-122">-DisplayName</span></span>
<span data-ttu-id="49d4c-123">Neuer Anzeigename für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="49d4c-123">New Display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d4c-124">-Startseite</span><span class="sxs-lookup"><span data-stu-id="49d4c-124">-HomePage</span></span>
<span data-ttu-id="49d4c-125">Neue URL der Anwendungsstartseite.</span><span class="sxs-lookup"><span data-stu-id="49d4c-125">New URL of the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d4c-126">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="49d4c-126">-IdentifierUris</span></span>
<span data-ttu-id="49d4c-127">Neue URIs, die die Anwendung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="49d4c-127">New URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d4c-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="49d4c-128">-ObjectId</span></span>
<span data-ttu-id="49d4c-129">Die Objekt-ID der zu aktualisierende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="49d4c-129">The object id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d4c-130">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="49d4c-130">-ReplyUrls</span></span>
<span data-ttu-id="49d4c-131">Neue Antwort-URLs für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="49d4c-131">New reply urls for the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49d4c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49d4c-132">-Confirm</span></span>
<span data-ttu-id="49d4c-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49d4c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49d4c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49d4c-134">-WhatIf</span></span>
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

### <span data-ttu-id="49d4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d4c-135">CommonParameters</span></span>
<span data-ttu-id="49d4c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d4c-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d4c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d4c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49d4c-138">INPUTS</span></span>

### <span data-ttu-id="49d4c-139">Keine</span><span class="sxs-lookup"><span data-stu-id="49d4c-139">None</span></span>
<span data-ttu-id="49d4c-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="49d4c-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49d4c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49d4c-141">OUTPUTS</span></span>

### <span data-ttu-id="49d4c-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="49d4c-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="49d4c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="49d4c-143">NOTES</span></span>

## <span data-ttu-id="49d4c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49d4c-144">RELATED LINKS</span></span>

[<span data-ttu-id="49d4c-145">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="49d4c-145">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="49d4c-146">Neu – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="49d4c-146">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="49d4c-147">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="49d4c-147">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="49d4c-148">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="49d4c-148">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="49d4c-149">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="49d4c-149">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="49d4c-150">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="49d4c-150">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

