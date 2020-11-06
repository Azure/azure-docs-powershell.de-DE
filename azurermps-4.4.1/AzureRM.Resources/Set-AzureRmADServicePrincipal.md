---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 67af78e767b8da7764053e3652e25aef53f2877e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500701"
---
# <span data-ttu-id="6633d-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6633d-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="6633d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6633d-102">SYNOPSIS</span></span>
<span data-ttu-id="6633d-103">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="6633d-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6633d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6633d-104">SYNTAX</span></span>

### <span data-ttu-id="6633d-105">SpObjectIdWithDisplayNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6633d-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6633d-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6633d-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6633d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6633d-107">DESCRIPTION</span></span>
<span data-ttu-id="6633d-108">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="6633d-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="6633d-109">Verwenden Sie New-AzureRmADSpCredential-Cmdlet, um die dem Dienstprinzipal zugeordneten Anmeldeinformationen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6633d-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="6633d-110">Verwenden Sie Set-AzureRmADApplication-Cmdlet, um die Eigenschaften zu aktualisieren, die der zugrunde liegenden Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6633d-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="6633d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6633d-111">EXAMPLES</span></span>

### <span data-ttu-id="6633d-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6633d-112">--------------------------  Example 1  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="6633d-113">Aktualisiert den Anzeigenamen für den Dienstprinzipal mit der angegebenen Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="6633d-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="6633d-114">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6633d-114">--------------------------  Example 2  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="6633d-115">Aktualisiert den Anzeigenamen für den Dienstprinzipal mit dem angegebenen Dienstprinzipalnamen.</span><span class="sxs-lookup"><span data-stu-id="6633d-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="6633d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6633d-116">PARAMETERS</span></span>

### <span data-ttu-id="6633d-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6633d-117">-DisplayName</span></span>
<span data-ttu-id="6633d-118">Neuer Anzeigename für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="6633d-118">New display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6633d-119">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="6633d-119">-ObjectId</span></span>
<span data-ttu-id="6633d-120">Die Objekt-ID des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6633d-120">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6633d-121">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6633d-121">-ServicePrincipalName</span></span>
<span data-ttu-id="6633d-122">Der SPN des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6633d-122">The SPN of service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6633d-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6633d-123">-Confirm</span></span>
<span data-ttu-id="6633d-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6633d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6633d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6633d-125">-WhatIf</span></span>
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

### <span data-ttu-id="6633d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6633d-126">-DefaultProfile</span></span>
<span data-ttu-id="6633d-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6633d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6633d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6633d-128">CommonParameters</span></span>
<span data-ttu-id="6633d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6633d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6633d-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6633d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6633d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6633d-131">INPUTS</span></span>

## <span data-ttu-id="6633d-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6633d-132">OUTPUTS</span></span>

## <span data-ttu-id="6633d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6633d-133">NOTES</span></span>

## <span data-ttu-id="6633d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6633d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6633d-135">Neu – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6633d-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="6633d-136">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6633d-136">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="6633d-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6633d-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="6633d-138">Satz-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="6633d-138">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="6633d-139">Neu – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6633d-139">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="6633d-140">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6633d-140">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

