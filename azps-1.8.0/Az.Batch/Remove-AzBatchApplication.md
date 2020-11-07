---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 2a449235ac2b3fa98357e91e15602a0c7bd9eedb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661665"
---
# <span data-ttu-id="fa915-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fa915-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="fa915-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa915-102">SYNOPSIS</span></span>
<span data-ttu-id="fa915-103">Löscht eine Anwendung aus einem Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="fa915-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="fa915-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa915-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa915-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa915-105">DESCRIPTION</span></span>
<span data-ttu-id="fa915-106">Das Cmdlet **Remove-AzBatchApplication** löscht eine Anwendung aus einem Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="fa915-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="fa915-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa915-107">EXAMPLES</span></span>

### <span data-ttu-id="fa915-108">Beispiel 1: Löschen einer Anwendung aus einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="fa915-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="fa915-109">Dieser Befehl löscht die Litware-Anwendung aus dem ContosoBatch-Konto.</span><span class="sxs-lookup"><span data-stu-id="fa915-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="fa915-110">Der Befehl schlägt fehl, wenn die Anwendung Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="fa915-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="fa915-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa915-111">PARAMETERS</span></span>

### <span data-ttu-id="fa915-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="fa915-112">-AccountName</span></span>
<span data-ttu-id="fa915-113">Gibt den Namen des Batch Kontos an, aus dem dieses Cmdlet eine Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="fa915-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa915-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fa915-114">-ApplicationId</span></span>
<span data-ttu-id="fa915-115">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="fa915-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa915-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa915-116">-DefaultProfile</span></span>
<span data-ttu-id="fa915-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa915-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa915-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa915-118">-ResourceGroupName</span></span>
<span data-ttu-id="fa915-119">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="fa915-119">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa915-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa915-120">CommonParameters</span></span>
<span data-ttu-id="fa915-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa915-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa915-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa915-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa915-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa915-123">INPUTS</span></span>

### <span data-ttu-id="fa915-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fa915-124">System.String</span></span>

## <span data-ttu-id="fa915-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa915-125">OUTPUTS</span></span>

### <span data-ttu-id="fa915-126">System. void</span><span class="sxs-lookup"><span data-stu-id="fa915-126">System.Void</span></span>

## <span data-ttu-id="fa915-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa915-127">NOTES</span></span>

## <span data-ttu-id="fa915-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa915-128">RELATED LINKS</span></span>

[<span data-ttu-id="fa915-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fa915-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="fa915-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fa915-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="fa915-131">Neu – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fa915-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="fa915-132">Neu – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fa915-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="fa915-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fa915-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="fa915-134">Satz-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fa915-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


