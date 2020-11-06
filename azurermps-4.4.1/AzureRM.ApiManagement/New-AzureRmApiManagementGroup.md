---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 8fc237b130e5044e52f47d306d04c42d12fbad81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498053"
---
# <span data-ttu-id="762a2-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="762a2-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="762a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="762a2-102">SYNOPSIS</span></span>
<span data-ttu-id="762a2-103">Erstellt eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="762a2-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="762a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="762a2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="762a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="762a2-105">DESCRIPTION</span></span>
<span data-ttu-id="762a2-106">Das Cmdlet **New-AzureRmApiManagementGroup** erstellt eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="762a2-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="762a2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="762a2-107">EXAMPLES</span></span>

### <span data-ttu-id="762a2-108">Beispiel 1: Erstellen einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="762a2-108">Example 1: Create a management group</span></span>
```
PS C:\>New-AzureRmApiManagementGroup -Context $APImContext -Name "Group0001"
```

<span data-ttu-id="762a2-109">Mit diesem Befehl wird eine Verwaltungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="762a2-109">This command creates a management group.</span></span>

## <span data-ttu-id="762a2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="762a2-110">PARAMETERS</span></span>

### <span data-ttu-id="762a2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="762a2-111">-Context</span></span>
<span data-ttu-id="762a2-112">Gibt die Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="762a2-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762a2-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="762a2-113">-Description</span></span>
<span data-ttu-id="762a2-114">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="762a2-114">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762a2-115">-Extern</span><span class="sxs-lookup"><span data-stu-id="762a2-115">-ExternalId</span></span>
<span data-ttu-id="762a2-116">Für externe Gruppen enthält diese Eigenschaft die ID der Gruppe des externen Identitätsanbieters, beispielsweise Azure Active Directory-Aad://contoso5api.onmicrosoft.com/Groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; Andernfalls ist der Wert NULL.</span><span class="sxs-lookup"><span data-stu-id="762a2-116">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a2-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="762a2-117">-GroupId</span></span>
<span data-ttu-id="762a2-118">Gibt den Bezeichner der neuen Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="762a2-118">Specifies the identifier of the new management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762a2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="762a2-119">-Name</span></span>
<span data-ttu-id="762a2-120">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="762a2-120">Specifies the management group name.</span></span>

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

### <span data-ttu-id="762a2-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="762a2-121">-Type</span></span>
<span data-ttu-id="762a2-122">Group-Typ.</span><span class="sxs-lookup"><span data-stu-id="762a2-122">Group Type.</span></span> <span data-ttu-id="762a2-123">Benutzerdefinierte Gruppe ist eine benutzerdefinierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="762a2-123">Custom Group is User defined Group.</span></span> <span data-ttu-id="762a2-124">Die System Gruppe umfasst Administrator, Entwickler und Gäste.</span><span class="sxs-lookup"><span data-stu-id="762a2-124">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="762a2-125">Es ist nicht möglich, eine System Gruppe zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="762a2-125">You cannot create or update a System Group.</span></span>  <span data-ttu-id="762a2-126">Externe Gruppe ist Gruppen von externen Identitätsanbietern wie Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="762a2-126">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="762a2-127">Dieser Parameter ist optional und wird standardmäßig als benutzerdefinierte Gruppe angenommen.</span><span class="sxs-lookup"><span data-stu-id="762a2-127">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762a2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762a2-128">-DefaultProfile</span></span>
<span data-ttu-id="762a2-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="762a2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="762a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762a2-130">CommonParameters</span></span>
<span data-ttu-id="762a2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762a2-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="762a2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762a2-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="762a2-133">INPUTS</span></span>

## <span data-ttu-id="762a2-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="762a2-134">OUTPUTS</span></span>

### <span data-ttu-id="762a2-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="762a2-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="762a2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="762a2-136">NOTES</span></span>

## <span data-ttu-id="762a2-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="762a2-137">RELATED LINKS</span></span>

[<span data-ttu-id="762a2-138">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="762a2-138">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="762a2-139">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="762a2-139">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="762a2-140">Satz-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="762a2-140">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


