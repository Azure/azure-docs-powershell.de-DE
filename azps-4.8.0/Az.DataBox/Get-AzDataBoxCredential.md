---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009937"
---
# <span data-ttu-id="cbf66-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="cbf66-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="cbf66-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cbf66-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf66-103">Ruft die Datenbox-Anmeldeinformationen eines bestimmten Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="cbf66-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="cbf66-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbf66-104">SYNTAX</span></span>

### <span data-ttu-id="cbf66-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cbf66-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbf66-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbf66-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbf66-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbf66-107">DESCRIPTION</span></span>
<span data-ttu-id="cbf66-108">Das Cmdlet " **Get-AzDataBoxCredential** " Ruft die Anmeldeinformationen der Datenbox eines bestimmten Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="cbf66-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="cbf66-109">Die internen Eigenschaften des zurückgegebenen Credentials-Objekts sind für verschiedene SKU-Typen unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="cbf66-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="cbf66-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cbf66-110">EXAMPLES</span></span>

### <span data-ttu-id="cbf66-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cbf66-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="cbf66-112">Diese gibt die JobSecrets des angegebenen Auftrags</span><span class="sxs-lookup"><span data-stu-id="cbf66-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="cbf66-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cbf66-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="cbf66-114">Diese gibt die JobSecrets des angegebenen Auftrags</span><span class="sxs-lookup"><span data-stu-id="cbf66-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="cbf66-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbf66-115">PARAMETERS</span></span>

### <span data-ttu-id="cbf66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf66-116">-DefaultProfile</span></span>
<span data-ttu-id="cbf66-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cbf66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbf66-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cbf66-118">-Name</span></span>
<span data-ttu-id="cbf66-119">DataBox-Auftrags Name</span><span class="sxs-lookup"><span data-stu-id="cbf66-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf66-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf66-120">-ResourceGroupName</span></span>
<span data-ttu-id="cbf66-121">Datenbox-Auftrags Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="cbf66-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf66-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cbf66-122">-ResourceId</span></span>
<span data-ttu-id="cbf66-123">DataBox-Auftrags Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="cbf66-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf66-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf66-124">CommonParameters</span></span>
<span data-ttu-id="cbf66-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf66-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf66-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbf66-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf66-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cbf66-127">INPUTS</span></span>

### <span data-ttu-id="cbf66-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cbf66-128">System.String</span></span>

## <span data-ttu-id="cbf66-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cbf66-129">OUTPUTS</span></span>

### <span data-ttu-id="cbf66-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Management. DataBox. Models. UnencryptedCredentials, Microsoft. Azure. Management. DataBox, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cbf66-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="cbf66-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cbf66-131">NOTES</span></span>

## <span data-ttu-id="cbf66-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cbf66-132">RELATED LINKS</span></span>
