---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 8f7d221ca4f90f67bce038015b4c654881dfa598
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996941"
---
# <span data-ttu-id="a4d37-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a4d37-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="a4d37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4d37-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d37-103">Erstellt eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a4d37-103">Creates an API management group.</span></span>

## <span data-ttu-id="a4d37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d37-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4d37-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4d37-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d37-106">Das Cmdlet **New-AzApiManagementGroup** erstellt eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a4d37-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="a4d37-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4d37-107">EXAMPLES</span></span>

### <span data-ttu-id="a4d37-108">Beispiel 1: Erstellen einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a4d37-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="a4d37-109">Mit diesem Befehl wird eine Verwaltungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4d37-109">This command creates a management group.</span></span>

## <span data-ttu-id="a4d37-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4d37-110">PARAMETERS</span></span>

### <span data-ttu-id="a4d37-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a4d37-111">-Context</span></span>
<span data-ttu-id="a4d37-112">Gibt die Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="a4d37-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d37-113">-DefaultProfile</span></span>
<span data-ttu-id="a4d37-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4d37-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4d37-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4d37-115">-Description</span></span>
<span data-ttu-id="a4d37-116">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a4d37-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="a4d37-117">-Extern</span><span class="sxs-lookup"><span data-stu-id="a4d37-117">-ExternalId</span></span>
<span data-ttu-id="a4d37-118">Für externe Gruppen enthält diese Eigenschaft die ID der Gruppe des externen Identitätsanbieters, beispielsweise Azure Active Directory-Aad://contoso5api.onmicrosoft.com/Groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; Andernfalls ist der Wert NULL.</span><span class="sxs-lookup"><span data-stu-id="a4d37-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="a4d37-119">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="a4d37-119">-GroupId</span></span>
<span data-ttu-id="a4d37-120">Gibt den Bezeichner der neuen Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a4d37-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="a4d37-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a4d37-121">-Name</span></span>
<span data-ttu-id="a4d37-122">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a4d37-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="a4d37-123">-Typ</span><span class="sxs-lookup"><span data-stu-id="a4d37-123">-Type</span></span>
<span data-ttu-id="a4d37-124">Group-Typ.</span><span class="sxs-lookup"><span data-stu-id="a4d37-124">Group Type.</span></span> <span data-ttu-id="a4d37-125">Benutzerdefinierte Gruppe ist eine benutzerdefinierte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a4d37-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="a4d37-126">Die System Gruppe umfasst Administrator, Entwickler und Gäste.</span><span class="sxs-lookup"><span data-stu-id="a4d37-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="a4d37-127">Es ist nicht möglich, eine System Gruppe zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a4d37-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="a4d37-128">Externe Gruppe ist Gruppen von externen Identitätsanbietern wie Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a4d37-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="a4d37-129">Dieser Parameter ist optional und wird standardmäßig als benutzerdefinierte Gruppe angenommen.</span><span class="sxs-lookup"><span data-stu-id="a4d37-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

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

### <span data-ttu-id="a4d37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d37-130">CommonParameters</span></span>
<span data-ttu-id="a4d37-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d37-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4d37-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d37-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4d37-133">INPUTS</span></span>

### <span data-ttu-id="a4d37-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a4d37-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a4d37-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d37-135">System.String</span></span>

### <span data-ttu-id="a4d37-136">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroupType, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a4d37-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a4d37-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4d37-137">OUTPUTS</span></span>

### <span data-ttu-id="a4d37-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a4d37-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="a4d37-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4d37-139">NOTES</span></span>

## <span data-ttu-id="a4d37-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4d37-140">RELATED LINKS</span></span>

[<span data-ttu-id="a4d37-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a4d37-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="a4d37-142">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a4d37-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="a4d37-143">Satz-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a4d37-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


