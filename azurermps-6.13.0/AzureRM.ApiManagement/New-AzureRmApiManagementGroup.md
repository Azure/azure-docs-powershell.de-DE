---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: c5bbe6413a17707e7c25a616c3c67d6b7d5da5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501249"
---
# <span data-ttu-id="d093b-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d093b-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="d093b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d093b-102">SYNOPSIS</span></span>
<span data-ttu-id="d093b-103">Erstellt eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d093b-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d093b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d093b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d093b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d093b-105">DESCRIPTION</span></span>
<span data-ttu-id="d093b-106">Das Cmdlet **New-AzureRmApiManagementGroup** erstellt eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d093b-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="d093b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d093b-107">EXAMPLES</span></span>

### <span data-ttu-id="d093b-108">Beispiel 1: Erstellen einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="d093b-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="d093b-109">Mit diesem Befehl wird eine Verwaltungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="d093b-109">This command creates a management group.</span></span>

## <span data-ttu-id="d093b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d093b-110">PARAMETERS</span></span>

### <span data-ttu-id="d093b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d093b-111">-Context</span></span>
<span data-ttu-id="d093b-112">Gibt die Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d093b-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d093b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d093b-113">-DefaultProfile</span></span>
<span data-ttu-id="d093b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d093b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d093b-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d093b-115">-Description</span></span>
<span data-ttu-id="d093b-116">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d093b-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="d093b-117">-Extern</span><span class="sxs-lookup"><span data-stu-id="d093b-117">-ExternalId</span></span>
<span data-ttu-id="d093b-118">Für externe Gruppen enthält diese Eigenschaft die ID der Gruppe des externen Identitätsanbieters, beispielsweise Azure Active Directory-Aad://contoso5api.onmicrosoft.com/Groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; Andernfalls ist der Wert NULL.</span><span class="sxs-lookup"><span data-stu-id="d093b-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="d093b-119">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="d093b-119">-GroupId</span></span>
<span data-ttu-id="d093b-120">Gibt den Bezeichner der neuen Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d093b-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="d093b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d093b-121">-Name</span></span>
<span data-ttu-id="d093b-122">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d093b-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="d093b-123">-Typ</span><span class="sxs-lookup"><span data-stu-id="d093b-123">-Type</span></span>
<span data-ttu-id="d093b-124">Group-Typ.</span><span class="sxs-lookup"><span data-stu-id="d093b-124">Group Type.</span></span> <span data-ttu-id="d093b-125">Benutzerdefinierte Gruppe ist eine benutzerdefinierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d093b-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="d093b-126">Die System Gruppe umfasst Administrator, Entwickler und Gäste.</span><span class="sxs-lookup"><span data-stu-id="d093b-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="d093b-127">Es ist nicht möglich, eine System Gruppe zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d093b-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="d093b-128">Externe Gruppe ist Gruppen von externen Identitätsanbietern wie Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d093b-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="d093b-129">Dieser Parameter ist optional und wird standardmäßig als benutzerdefinierte Gruppe angenommen.</span><span class="sxs-lookup"><span data-stu-id="d093b-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d093b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d093b-130">CommonParameters</span></span>
<span data-ttu-id="d093b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d093b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d093b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d093b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d093b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d093b-133">INPUTS</span></span>

### <span data-ttu-id="d093b-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d093b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d093b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d093b-135">System.String</span></span>

### <span data-ttu-id="d093b-136">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroupType, Microsoft. Azure. Commands. ApiManagement. Servicemanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d093b-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d093b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d093b-137">OUTPUTS</span></span>

### <span data-ttu-id="d093b-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d093b-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="d093b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d093b-139">NOTES</span></span>

## <span data-ttu-id="d093b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d093b-140">RELATED LINKS</span></span>

[<span data-ttu-id="d093b-141">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d093b-141">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d093b-142">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d093b-142">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d093b-143">Satz-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d093b-143">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


