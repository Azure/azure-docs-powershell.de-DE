---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009462"
---
# <span data-ttu-id="9c3ab-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="9c3ab-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="9c3ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3ab-103">Ruft einen geheimen Wert des angegebenen benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="9c3ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c3ab-104">SYNTAX</span></span>

### <span data-ttu-id="9c3ab-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c3ab-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c3ab-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="9c3ab-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c3ab-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c3ab-107">DESCRIPTION</span></span>
<span data-ttu-id="9c3ab-108">Ruft einen geheimen Wert des angegebenen benannten Werts ab.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="9c3ab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c3ab-109">EXAMPLES</span></span>

### <span data-ttu-id="9c3ab-110">Beispiel 1: Abrufen des benannten Werts nach Name</span><span class="sxs-lookup"><span data-stu-id="9c3ab-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="9c3ab-111">Dieser Befehl ruft die Details des benannten Werts ab, wobei der Name des benannten Werts angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="9c3ab-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c3ab-112">PARAMETERS</span></span>

### <span data-ttu-id="9c3ab-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9c3ab-113">-Context</span></span>
<span data-ttu-id="9c3ab-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9c3ab-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9c3ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3ab-116">-DefaultProfile</span></span>
<span data-ttu-id="9c3ab-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c3ab-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="9c3ab-118">-NamedValueId</span></span>
<span data-ttu-id="9c3ab-119">Der Bezeichner des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-119">Identifier of a the named value.</span></span>
<span data-ttu-id="9c3ab-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3ab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3ab-121">CommonParameters</span></span>
<span data-ttu-id="9c3ab-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3ab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3ab-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c3ab-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3ab-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c3ab-124">INPUTS</span></span>

### <span data-ttu-id="9c3ab-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9c3ab-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9c3ab-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9c3ab-126">System.String</span></span>

## <span data-ttu-id="9c3ab-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c3ab-127">OUTPUTS</span></span>

### <span data-ttu-id="9c3ab-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="9c3ab-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="9c3ab-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c3ab-129">NOTES</span></span>

## <span data-ttu-id="9c3ab-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c3ab-130">RELATED LINKS</span></span>
