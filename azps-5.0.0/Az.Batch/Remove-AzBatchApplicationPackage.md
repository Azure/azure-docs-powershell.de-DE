---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177279"
---
# <span data-ttu-id="b4732-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b4732-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="b4732-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4732-102">SYNOPSIS</span></span>
<span data-ttu-id="b4732-103">Löscht einen Anwendungspaket-Datensatz und die binäre Datei.</span><span class="sxs-lookup"><span data-stu-id="b4732-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="b4732-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4732-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4732-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4732-105">DESCRIPTION</span></span>
<span data-ttu-id="b4732-106">Das Cmdlet **Remove-AzBatchApplicationPackage** löscht einen Anwendungspaket Eintrag und die Binärdatei aus einem Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="b4732-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="b4732-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4732-107">EXAMPLES</span></span>

### <span data-ttu-id="b4732-108">Beispiel 1: Löschen eines Anwendungspakets aus einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="b4732-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="b4732-109">Dieser Befehl löscht Version 1,0 der Litware-Anwendung aus dem ContosoBatchGroup-Konto.</span><span class="sxs-lookup"><span data-stu-id="b4732-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="b4732-110">Der Befehl löscht sowohl den paketdatensatz als auch das BLOB, das die binäre Paketdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="b4732-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="b4732-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4732-111">PARAMETERS</span></span>

### <span data-ttu-id="b4732-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b4732-112">-AccountName</span></span>
<span data-ttu-id="b4732-113">Gibt den Namen des Batch Kontos an, von dem dieses Cmdlet ein Anwendungspaket löscht.</span><span class="sxs-lookup"><span data-stu-id="b4732-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="b4732-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="b4732-114">-ApplicationName</span></span>
<span data-ttu-id="b4732-115">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="b4732-115">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4732-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="b4732-116">-ApplicationVersion</span></span>
<span data-ttu-id="b4732-117">Gibt die Version der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="b4732-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4732-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4732-118">-DefaultProfile</span></span>
<span data-ttu-id="b4732-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4732-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4732-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4732-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4732-121">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="b4732-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="b4732-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4732-122">CommonParameters</span></span>
<span data-ttu-id="b4732-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4732-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4732-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4732-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4732-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4732-125">INPUTS</span></span>

### <span data-ttu-id="b4732-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b4732-126">System.String</span></span>

## <span data-ttu-id="b4732-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4732-127">OUTPUTS</span></span>

### <span data-ttu-id="b4732-128">System. void</span><span class="sxs-lookup"><span data-stu-id="b4732-128">System.Void</span></span>

## <span data-ttu-id="b4732-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4732-129">NOTES</span></span>

## <span data-ttu-id="b4732-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4732-130">RELATED LINKS</span></span>

[<span data-ttu-id="b4732-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b4732-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="b4732-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b4732-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="b4732-133">Neu – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b4732-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="b4732-134">Neu – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b4732-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="b4732-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b4732-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="b4732-136">Satz-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b4732-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


