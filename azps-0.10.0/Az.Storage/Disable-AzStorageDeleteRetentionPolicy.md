---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f09ba3cdd0404f1eca21540a6893f1bcd67f05e5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843135"
---
# <span data-ttu-id="86072-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86072-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="86072-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86072-102">SYNOPSIS</span></span>
<span data-ttu-id="86072-103">Deaktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="86072-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="86072-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86072-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86072-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86072-105">DESCRIPTION</span></span>
<span data-ttu-id="86072-106">Das Cmdlet **Disable-AzStorageDeleteRetentionPolicy** deaktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="86072-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="86072-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86072-107">EXAMPLES</span></span>

### <span data-ttu-id="86072-108">Beispiel 1: Deaktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="86072-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="86072-109">Mit diesem Befehl wird die Aufbewahrungsrichtlinie für den BLOB-Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="86072-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="86072-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="86072-110">PARAMETERS</span></span>

### <span data-ttu-id="86072-111">-Context</span><span class="sxs-lookup"><span data-stu-id="86072-111">-Context</span></span>
<span data-ttu-id="86072-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="86072-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86072-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86072-113">-DefaultProfile</span></span>
<span data-ttu-id="86072-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86072-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86072-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86072-115">-PassThru</span></span>
<span data-ttu-id="86072-116">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="86072-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="86072-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86072-117">-Confirm</span></span>
<span data-ttu-id="86072-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86072-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86072-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86072-119">-WhatIf</span></span>
<span data-ttu-id="86072-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86072-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86072-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86072-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86072-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86072-122">CommonParameters</span></span>
<span data-ttu-id="86072-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86072-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86072-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86072-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86072-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86072-125">INPUTS</span></span>

### <span data-ttu-id="86072-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="86072-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="86072-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86072-127">OUTPUTS</span></span>

### <span data-ttu-id="86072-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86072-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="86072-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="86072-129">NOTES</span></span>

## <span data-ttu-id="86072-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86072-130">RELATED LINKS</span></span>
